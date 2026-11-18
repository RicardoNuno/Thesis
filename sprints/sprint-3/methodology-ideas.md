# Methodology: Watchdog

## Idea

The phone is a distraction even when it is only close by. Watchdog tries to replace it with a smartwatch, step by step, through three modes.

## Setup

1. **Goal:** the user states why they installed Watchdog.
2. **Allowlist:** the user chooses essentials that open without the launcher.
3. **Flagged apps:** the user chooses apps that he wants to cut down. They still open, but with more friction.
4. **Notifications:** the user chooses which apps notify in real time, and when batches are delivered.

These choices are made at install because that is when motivation is highest. Later, in a moment of temptation, the same user would choose looser rules. To protect the choices made at setup, loosening any setting afterwards takes effect only after 72 hours and must then be confirmed again, while tightening applies immediately. Every change is logged. After the first week, Watchdog can also suggest apps to flag from the logged data.

## Modes

### Shared by all modes

```
Notification arrives
  ├─ allowlisted app ──► shown now
  └─ other app ────────► held, delivered in the next batch

User unlocks the phone
  └─► AI launcher: "What do you want to do?"
        ├─ closes without an intention ──► logged as an empty check
        ├─ opens an allowlisted app ─────► opens directly (e.g. contacts, calls)
        └─ states an intention ──────────► AI opens the matching app (later: feature)
                                              └─► time box starts (e.g. 3 min for "reply to Ana")
                                                    ├─ long continuous scrolling ──► bypass prompt earlier
                                                    └─ time box ends ──► phone locks

App opened without the launcher (a notification, a link)
  └─► Bypass prompt: deliberate action required
        ├─ action done ──► app continues
        └─ not done ─────► back to the launcher

Everything above is logged ──► reports, streaks, goals, badges
```

**Interaction-level monitoring:** Watchdog detects scrolling and tapping inside apps, not only which app is open. Tapping and typing usually mean active use (replying, searching); long, continuous scrolling usually means a feed. Active tasks keep their full time box; continuous scrolling triggers the bypass prompt earlier.

### 1. No smartwatch

**Question:** Does stating an intention before opening an app reduce automatic checking and app-hopping?

Everything above runs on the phone.

- **Bypass prompt:** Type a new code in the phone in order to continue usage.

### 2. Smartwatch without LTE

**Question:** Does shifting the user's focus from the phone to the watch, through added friction, reduce phone time and pick-ups further than mode 1?

- **Connection:** watch paired with the phone over Bluetooth.
- **Launcher on the wrist:** the intention is stated on the watch, and the phone opens the matching app or feature.
- **Bypass prompt on the wrist:** the deliberate action is done on the watch: rotating the crown, a gesture, or another watch sensor. It still changes every time.
- **Haptic feedback:** the watch vibrates when a time box or limit runs out.
- **Live usage on the watch face:** today's pick-ups and phone time, always visible.
- **Fallback to mode 1:** when Bluetooth drops, or the watch is off the wrist or charging.

### 3. Smartwatch with LTE

**Question:** Which everyday tasks must work on the watch before the phone can be left behind entirely?

The watch works without the phone; everything from mode 2 still applies.

- **Enrolment:** the user chooses which essentials go on the watch, and the credentials they need are synced from the phone.
- **Wrist launcher:** the essentials are gathered in one curated launcher. Each task is an intent (e.g. "book a taxi", "pay"), handled by the same intent engine as the phone launcher.
- **Fallback:** to mode 1 when the watch is off the wrist or charging.

## Architecture

```
Phone app (Android)
├── Launcher           default home app: prompt, allowlist, time boxes
├── Intent engine      on-device model or rule-based matcher: intention → app / feature
├── Monitoring         UsageStatsManager, screen/unlock broadcasts; Accessibility service for scroll/tap events
├── Friction           overlay (bypass prompt), foreground service
├── Notifications      NotificationListenerService: real-time allowlist, batching
└── Local storage      Room DB, no cloud by default

Watch app (Wear OS)
├── Launcher           voice intention → opens app/feature on the phone (mode 2)
├── Friction           unlock confirmation, crown, haptics, watch face
└── Essentials         standalone apps over LTE (mode 3)
```

Phone ↔ watch: Wear OS Data Layer. Permissions: default home app, usage access, display over other apps, notification access, accessibility service (scroll/tap events).

## Signal sources: what each can see

Scrolling and tapping can be detected in three ways on Android. Part of the work is to test all three on real devices and compare them.

- **Usage stats:** which app is open and for how long. No scrolling or tapping. Needs only usage access.
- **Accessibility service:** every scroll and tap, the app it happened in, and the type of element. Needs the user to enable it in Settings; high privacy cost; strict Play Store rules.
- **ADB / Shizuku:** raw touch input, frames drawn, the current screen inside an app. Sees the most, but needs developer setup and must be restarted after every reboot.

For each source: what it detects, battery cost, setup effort, and privacy impact.

## Development

- **Stack:** Kotlin, Jetpack Compose, Room (phone); Compose for Wear OS (watch); Wear OS Data Layer between them.
- **Intent engine:** rule-based matcher first; on-device language model added where the device supports it. No cloud by default.
- **Order:** mode 1 first, then mode 2, then mode 3. Each mode is usable on its own before the next one starts.
- **Process:** iterative, monitoring layer first and then the intervention; tested on real devices across at least two Android versions; development log kept in this repository.

## Evaluation

- **Logged:** pick-ups, app opens, session length, app switches per session, screen time; phone and watch use logged together.
- **Questionnaires:** SAS-SV before/after, motivation to change, SUS (usability), acceptability.
- **Technical:** accuracy vs Digital Wellbeing, battery (phone and watch), launch delay.
- **Baseline:** Digital Wellbeing.
