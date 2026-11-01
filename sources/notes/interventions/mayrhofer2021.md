# mayrhofer2021: The Android Platform Security Model

**Authors / venue / year:** Mayrhofer, Vander Stoep, Brubaker & Kralevich (Google) / ACM Transactions on Privacy and Security 24(3), Article 19, 1–35 / 2021
**Link:** https://doi.org/10.1145/3448609 (preprint matching the published version: https://arxiv.org/abs/1904.05572v2; a 2023 update with more authors is v3)
**Relevance:** medium

_Read from arXiv v2 (Dec 2020, based on Android 11), which matches the published version; quotes cite sections._

## Summary (3 sentences)

Google engineers write down, for the first time, the security model behind Android: five rules, the central one being multi-party consent, meaning an action happens only if the user, the platform and the app developer all agree, and any of them can veto it. Apps are treated as separate security principals rather than as agents acting with the user's full rights, so one app cannot read or act on another app's data just because the user allows it. The paper then maps how permissions, the app sandbox (per-app UID, SELinux), authentication, encryption, exploit mitigation, verified boot and updates enforce this model, how it evolved from Android 4 to 11, and which special cases deviate from it.

## Method

- Informal systematisation by platform designers, not an empirical study: ecosystem context, a layered threat model (physical, network, untrusted code, untrusted content), the five rules, then implementation per layer with tables of security changes per Android release (4.x–11), and special cases.
- Scope is AOSP only; Google Play policies, Play Protect and Google Mobile Services are explicitly out of scope.

## Results / evidence

- **Five rules:** (1) multi-party consent (user, platform, developer); (2) open ecosystem (sideloading and other stores allowed, apps can expose APIs to each other); (3) security is a compatibility requirement (rooted devices are not "Android" under the CDD); (4) factory reset restores a safe state; (5) applications are security principals.
- **Three access-control mechanisms, one per party:** the platform uses mandatory access control (SELinux), apps use discretionary access control (UNIX permissions, URI grants), users grant Android permissions.
- **Five permission classes:** normal (auto-granted at install), runtime/dangerous (prompt during use), **special access** (cannot be requested with a prompt; the user must go to Settings, e.g. device admin, notification listener, installing packages), privileged (pre-installed apps only), signature (same signing key only).
- **Changes relevant to monitoring apps:** runtime permissions (Android 6); `SYSTEM_ALERT_WINDOW` (overlays) moved to special access (Android 6); `hidepid=2` removed the `/proc` side channel apps used to infer when other apps start (Android 7); "allow only while using the app" permissions (Android 10) and one-time permissions (Android 11); background activity starts restricted to visible windows or specific exceptions (Android 10); clipboard only readable by the focused app (Android 10); scoped storage; package visibility limited, `QUERY_ALL_PACKAGES` needed (Android 11).
- **Accessibility:** listed among user-consent lessons: "restrictions to accessibility service APIs (which require user consent but were abused)"; UI deception (`SYSTEM_ALERT_WINDOW`, background activity limits) handled by Play checks and platform restrictions.
- **User-consent principles:** avoid over-prompting (prompt fatigue), prompt in understandable terms, prefer pickers and transactional consent over broad grants, don't offload hard decisions to users, make decisions undoable.
- **Special cases:** listing installed packages, VPN apps seeing other apps' traffic (allowed because the user value and consent are clear), backup, enterprise Device Owner/Profile Owner policies as a fourth consenting party, factory reset protection.
- Lockscreen context: users unlock about 50 times a day (up to 200) for short 10–250 s sessions; tiered unlock (knowledge factor, biometrics with a 72 h fallback, trusted devices/places with a 4 h fallback).

## Strengths / limitations

- Strength: authoritative explanation of why Android restricts what apps can see and do, with a version-by-version table of the changes.
- Strength: names the consent principles behind permission design, which can be used to judge an app's onboarding.
- Limitation: written by Google employees about their own product, with internal unpublished figures (e.g. lockscreen adoption); it explains the design rather than evaluating it critically.
- Limitation: Play Store policy, where most restrictions on Accessibility and usage access actually bite for third-party apps, is out of scope.
- Limitation: snapshot of Android 11; restrictions added since (e.g. Android 13 restricted settings for sideloaded apps) are not covered.
- Limitation: `PACKAGE_USAGE_STATS` (usage access) is never discussed by name, though it belongs to the special access class described.

## How it relates to my thesis

Gives the formal reason behind the constraints any Android wellbeing app runs into: under multi-party consent, an app that watches or alters other apps acts on data those developers control, so Android routes such capabilities (usage access, overlays, notification listeners, Accessibility) through high-friction special access or restricted APIs, and has closed side channels like `/proc`. This frames the technical survey part of my proposal: each monitoring or intervention API (cf. lu2024's Accessibility overlay, datta2022's overlay and ADB, okeke2018's foreground-app check) can be placed in a permission class with its consent cost. Its user-consent principles (no over-prompting, understandable prompts, undoable decisions) are a ready basis for designing consent-friendly onboarding and permission requests, and the restriction on background activity starts limits how an intervention screen can be launched. The Device Owner/Profile Owner case also explains how parental-control and work-profile tools get stronger control.

## Quotes / figures worth citing (with section)

- "Multi-party consent. No action should be executed unless all main parties agree — in the standard case, these are user, platform, and developer ... Any one party can veto the action." (§3, rule 1)
- "Android apps are not considered to be fully authorized agents for user actions." (§3, rule 5)
- "In order for a user to allow an application to use a special access permission, the user must go to settings and manually grant the permission to the application." (§4.3.1)
- "Over-prompting the user leads to prompt fatigue and blindness" (§4.1.3)
- "restrictions to accessibility service APIs (which require user consent but were abused)" (§4.1.3)
- "users unlock phones for short (10-250 seconds) interactions about 50 times per day on average and even up to 200 times in exceptional cases" (§4.2)
- Table 1: application sandboxing improvements per Android release (§4.3.2).
