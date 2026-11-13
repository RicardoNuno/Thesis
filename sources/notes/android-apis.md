# Android monitoring and intervention APIs

This note compares the Android mechanisms a well-being app can use to **monitor** phone use and to **intervene** on it. For each one it covers the data it gives, the permission it needs, its privacy impact and the risk of a Google Play policy problem. It is the technical part of the State of the Art (synthesis §1.11).

The permission classes follow mayrhofer2021:
- **normal**: granted automatically at install
- **runtime**: the app asks with a system prompt
- **special access**: the user has to switch it on by hand in Settings
- **privileged / signature**: only for system or pre-installed apps

Facts taken from the Android documentation or Google Play policy rather than from a paper cite a source as [Dn]; the list is at the end. They were checked on 13 Nov 2026.

---

## Comparison table

| # | Mechanism | Monitor / intervene | Data or capability | Permission (class, how granted) | Privacy impact | Play Store risk | Accuracy | Battery | Used in |
|---|-----------|---------------------|--------------------|---------------------------------|----------------|-----------------|----------|---------|---------|
| 1 | **UsageStatsManager / UsageEvents** | Monitor | Foreground app start/end (`ACTIVITY_RESUMED/PAUSED`, API 29+), screen on/off and keyguard events (API 28+) [D1]; per-app aggregates by day, week, month and year [D2] | `PACKAGE_USAGE_STATS`: special access (appop; Settings → Usage access) [D3] | Medium: which apps are used and when, no content | Low: not on Play's list of permissions that need a declaration [D4] | High for app time and unlocks. Raw events are "only kept by the system for a few days" [D2], so the app has to copy them regularly | Very low: read on demand, no service needed | shahu2024; leiva2012 and bohmer2011 (modern equivalent) |
| 2 | **Screen and unlock broadcasts** (`ACTION_SCREEN_ON/OFF`, `ACTION_USER_PRESENT`) | Monitor | Screen-on and unlock moments, i.e. pick-ups | None. SCREEN_ON/OFF can only be received by a receiver registered at runtime [D5]. USER_PRESENT is not on the implicit-broadcast exceptions list, so the same applies for apps targeting API 26+ [D6]. A process has to stay alive | Low | Low | High for pick-ups while the process is alive | Low on its own; the real cost is the foreground service (#9) | mehrotra2016 (unlock = "seen"), ferreira2014 |
| 3 | **NotificationListenerService** | Both | Every posted and removed notification: app, time, title/text, actions. Can also cancel or snooze them (snooze from API 26) [D7] | Special access (Settings → Notification access) [D8]. Apps sideloaded from a file or a browser hit "restricted settings" (Android 13+) and need App info → "Allow restricted settings" first [D9, D10] | **High**: reads message contents from every app | Medium: needs a disclosure; must not exfiltrate content | High | Low: the system binds the service on events | mehrotra2016, pielot2014 (accessibility API then) |
| 4 | **AccessibilityService** | Both | Window changes (foreground app), on-screen view tree and text, UI events. Can draw `TYPE_ACCESSIBILITY_OVERLAY` and inject gestures (`dispatchGesture`) | Special access (Settings → Accessibility) plus restricted settings for sideloaded apps [D9, D10]; abuse led to tightening (mayrhofer2021) | **Very high**: can see and act on everything on screen | **High**: apps that are not accessibility tools need a prominent disclosure with consent and a Play Console declaration that Google approves. Fixed, rule-based automation is allowed; autonomous decision-making is not [D11]. lu2024 also flags this risk | Very high, even below app level (screens, features) | Medium: depends on the event types and how much of the view tree it reads | lu2024, ferreira2014 (AWARE), okeke2018-style foreground checks |
| 5 | **Overlay window** (`SYSTEM_ALERT_WINDOW`) | Intervene | Draws a view over other apps: friction screen, pause, timer, banner | Special access (Settings → Display over other apps) for apps targeting API 23 / Android 6+ [D12] (mayrhofer2021) | Low on its own: it cannot see what's underneath | Medium: policy against deceptive or disruptive overlays. Since Android 12, touches that pass through an overlay with opacity above 0.8 are blocked; a full-screen pause screen that takes the touches itself is not affected [D13] | n/a; needs #1 or #4 to know when to show | Low while hidden | datta2022, kim2019lockntype, haliburton2024 (one sec-style pause) |
| 6 | **Home-screen app (launcher)** | Intervene (monitors only its own launches) | Controls how apps are shown and launched: hide apps, text-only list, intention prompt before opening | Becoming the default Home app (user choice in Settings). To list apps, declare a `<queries>` entry for the MAIN/LAUNCHER intent [D14]. `QUERY_ALL_PACKAGES` needs Play approval, and launchers are not among its permitted uses [D15] | Low | Low | Sees only launches from itself, so it misses opens from notifications, recents and links | Very low | schraggeova2025 (MinimalistPhone), olson2022nudge (hiding apps) |
| 7 | **Notification policy / Do Not Disturb** (`NotificationManager`, `AutomaticZenRule`) | Intervene | Turns DND on or off, sets which interruptions are allowed and schedules rules | `ACCESS_NOTIFICATION_POLICY` is a normal "marker" permission; the real grant is special access (Settings → Do Not Disturb / Modes access) [D16]. Apps targeting API 35+ can no longer change the global filter, only their own `AutomaticZenRule` [D17] | Low | Low | n/a | Very low | Related to olson2022nudge (turning notifications off) |
| 8 | **Device policy** (`DevicePolicyManager`) | Intervene | Strong control, e.g. suspending or hiding apps and lock-task mode | Specific device-admin policies were deprecated from Android 9 and blocked from Android 10 [D18]. Suspending or hiding apps needs **device owner** or **profile owner** [D19]. Device owner can only be set at initial setup or after a factory reset (QR code, NFC, zero-touch, or ADB on a phone with no accounts) [D20]. A profile owner (work profile) can be added later | High: control over the whole device | High outside managed devices | n/a | Low | None in the reading; parental-control apps |
| 9 | **Foreground service** | Enabler | Keeps a process running so it can poll, keep receivers alive and time sessions | `FOREGROUND_SERVICE` (normal). Apps targeting Android 14+ must declare a type and its permission; `specialUse` also needs a written justification that Play reviews [D21]. `POST_NOTIFICATIONS` is a runtime permission from Android 13 [D22] | Low, but the ongoing notification is always visible | Medium: the `specialUse` declaration gets reviewed | n/a | **Medium–high**: the main battery cost of any always-on design | okeke2018 (foreground-app checks), shahu2024 |
| 10 | **Local VPN** (`VpnService`) | Both | Sees and can block network traffic per domain, e.g. feeds or sites | Consent dialog via `VpnService.prepare()`; only one VPN can run at a time [D23] | **Very high**: all network traffic | **High**: Play allows VpnService for core VPN apps and listed exceptions, which include parental control and app usage tracking. All need a declaration with demo and disclosure videos, a note in the store listing, and encrypted traffic to the tunnel endpoint [D24] | Medium: works at domain level, not per feature | Medium | None in the reading |
| 11 | **Screen capture** (`MediaProjection`, or ADB) | Monitor | Raw screen frames for OCR or ML detection of features | MediaProjection: consent dialog before every session from Android 14, plus a `mediaProjection` foreground service when targeting 14+. A status-bar chip is shown from Android 15 QPR1 [D25]. ADB: developer-level grant | **Very high**: everything on screen | High | High for feature detection, but slow | **High**: capture plus inference (60–120 s per frame on-device in datta2022) | datta2022 (ADB, research only) |
| 12 | **Wear OS Data Layer** | Both (via the watch) | Syncs data between phone and watch; the watch face and vibration act as the feedback channel | None for syncing; both apps need the same package name and signing key [D26]. Heart rate needs `BODY_SENSORS` up to Wear OS 5.1, `health.READ_HEART_RATE` from Wear OS 6 [D27] | Low–medium | Low | Depends on the phone side (#1) | Watch battery suffers from frequent wake-ups (liu2017) | shahu2024 |
| — | **Closed routes** | — | `ActivityManager.getRunningTasks` (deprecated, closed to third-party apps since Android 5; returns little beyond the caller's own tasks [D28]), `/proc` side channel (closed in Android 7, mayrhofer2021), root, app patching | — | — | — | — | — | datta2022 (map of options), older logging studies |

---

## Sources

- [D1] UsageEvents.Event: https://developer.android.com/reference/android/app/usage/UsageEvents.Event
- [D2] UsageStatsManager: https://developer.android.com/reference/android/app/usage/UsageStatsManager
- [D3] PACKAGE_USAGE_STATS: https://developer.android.com/reference/android/Manifest.permission#PACKAGE_USAGE_STATS
- [D4] Play permissions policy: https://support.google.com/googleplay/android-developer/answer/9888170
- [D5] ACTION_SCREEN_ON: https://developer.android.com/reference/android/content/Intent#ACTION_SCREEN_ON
- [D6] Implicit broadcast exceptions: https://developer.android.com/guide/components/broadcast-exceptions
- [D7] NotificationListenerService: https://developer.android.com/reference/android/service/notification/NotificationListenerService
- [D8] ACTION_NOTIFICATION_LISTENER_SETTINGS: https://developer.android.com/reference/android/provider/Settings#ACTION_NOTIFICATION_LISTENER_SETTINGS
- [D9] Restricted settings (Google Help): https://support.google.com/android/answer/12623953
- [D10] Android 16 CDD §9.8 (restricted settings for accessibility and notification access): https://source.android.com/docs/compatibility/16/android-16-cdd
- [D11] Play AccessibilityService API policy: https://support.google.com/googleplay/android-developer/answer/10964491
- [D12] SYSTEM_ALERT_WINDOW: https://developer.android.com/reference/android/Manifest.permission#SYSTEM_ALERT_WINDOW
- [D13] Android 12 untrusted touch events: https://developer.android.com/about/versions/12/behavior-changes-all#untrusted-touch-events
- [D14] Package visibility: https://developer.android.com/training/package-visibility
- [D15] Play QUERY_ALL_PACKAGES policy: https://support.google.com/googleplay/android-developer/answer/10158779
- [D16] ACCESS_NOTIFICATION_POLICY: https://developer.android.com/reference/android/Manifest.permission#ACCESS_NOTIFICATION_POLICY
- [D17] NotificationManager.setInterruptionFilter: https://developer.android.com/reference/android/app/NotificationManager#setInterruptionFilter(int)
- [D18] Device admin deprecation: https://developers.google.com/android/work/device-admin-deprecation
- [D19] DevicePolicyManager: https://developer.android.com/reference/android/app/admin/DevicePolicyManager
- [D20] Provisioning: https://developers.google.com/android/work/prov-devices
- [D21] Foreground service types: https://developer.android.com/develop/background-work/services/fgs/service-types
- [D22] POST_NOTIFICATIONS: https://developer.android.com/reference/android/Manifest.permission#POST_NOTIFICATIONS
- [D23] VpnService: https://developer.android.com/reference/android/net/VpnService
- [D24] Play VpnService policy: https://support.google.com/googleplay/android-developer/answer/12564964
- [D25] MediaProjection: https://developer.android.com/media/grow/media-projection
- [D26] Wear OS Data Layer: https://developer.android.com/training/wearables/data/overview
- [D27] Health Services permissions: https://developer.android.com/health-and-fitness/guides/health-services/permissions
- [D28] ActivityManager.getRunningTasks: https://developer.android.com/reference/android/app/ActivityManager#getRunningTasks(int)
