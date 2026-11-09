# bolle2015: Optimizing Smartphone Micro-usage with Smartwatch Notifications

**Authors / venue / year:** Bolle, De Croon & Duval / MobileHCI '15 Adjunct, 947–950 / 2015
**Link:** https://doi.org/10.1145/2786567.2794313 (open access: https://lirias.kuleuven.be/handle/123456789/505961)
**Relevance:** low

## Summary (3 sentences)

Short adjunct paper testing whether handling notifications on a smartwatch can cut "micro-usage" (brief phone sessions, mostly triggered by notifications from messaging apps). After logging 14 students' phones for a week (75% of app launches were micro-usage; 47% of screen-on sessions under 15 s), the authors compared three ways to act on notifications on an Android Wear watch and built "WearNotifier", which splits the watch screen into four quick actions (e.g., delete, reply, remind later) for SMS and IMAP email. Eight students used it for 3–4 days: overall phone screen sessions that were micro-usage fell 5% while app-level micro-usage rose 5%, with good usability (SUS 80) and perceived usefulness rising from 3.2 to 3.9 out of 5.

## Method

- Baseline: 14 students' phone use for one week via the AWARE framework; top apps by sessions Facebook (3,148), Messenger (1,900), SMS (1,613), WhatsApp (1,453), Snapchat (953).
- Lab comparison (5 students, one task: set a 2-hour reminder for a notification): four-quadrant buttons, double-tapping the watch's sides, drawn gestures, vs standard Android Wear (10.43 s); measured time and perceived usefulness (Davis).
- Field test: WearNotifier (quadrant design) on a Samsung Gear Live, 8 male students aged 22–24, 3–4 days each; AWARE logging, action logs, usefulness questionnaire before/after, SUS.

## Results / evidence

- Lab: quadrant buttons 16% faster than standard, drawn gestures 2% faster, edge taps 8% slower; quadrants rated most useful.
- Field: perceived usefulness 3.2 → 3.9; SUS 80 ("good" to "excellent"); the reminder action was more useful than expected.
- General smartphone micro-sessions −5%, "presumably because some notifications can be entirely handled on the smartwatch"; app micro-usage +5%, perhaps because users no longer read the content on the phone and only open apps briefly to act.

## Strengths / limitations

- Strength: an early concrete test of moving notification handling from phone to watch, with logging rather than self-report.
- Limitation: very small and short (8 men, 3–4 days); no statistics.
- Limitation: the ±5% comparison is against a different group (the 14 baseline students), not the same participants before and after; no watch-without-app condition (acknowledged).
- Limitation: only SMS and IMAP email, while most notifications in the baseline came from Facebook, Messenger and WhatsApp; no qualitative data to explain results.

## How it relates to my thesis

Supports the notification-triage mechanism behind the smartwatch idea (cecchinato2017, shahu2024): if a notification can be fully handled on the watch, the phone does not need to be unlocked, which is where micro-usage turns into longer sessions (ferreira2014, oulasvirta2012). The effect it measured is small and weakly evidenced, so it is at most an illustration; the design lesson is that watch actions must cover the apps that generate most notifications (messaging), otherwise the phone is still needed.

## Quotes / figures worth citing (with page)

- "smartphones have very limited potential for micro-interactions, which leads to users being mired and head-down in their touch screens." (quoting Starner, p. 947)
- "In our study with students, 75% of application launches resulted in micro-usage." (p. 948)
- "General smartphone micro-sessions (screen on until screen off), however, decreased by 5%, presumably because some notifications can be entirely handled on the smartwatch." (p. 950)
- Table 1: sessions of top 5 apps (p. 948). Figs. 2–4: three interaction proposals (p. 949).
