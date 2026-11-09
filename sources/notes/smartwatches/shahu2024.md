# shahu2024: Beyond Screen Time: Exploring Smartwatch Interventions for Digital Well-Being

**Authors / venue / year:** Shahu, Pechstein & Michahelles / Mensch und Computer (MuC '24), 83–98 / 2024
**Link:** https://doi.org/10.1145/3670653.3670674 (open access; also TU Wien repositum)
**Relevance:** high

## Summary (3 sentences)

The authors built "Watchful", an Android phone app plus a Wear OS watch app: the phone collects usage with UsageStatsManager, the watch face shows today's screen time, unlocks and a colour-coded doughnut of the top apps, and when a user-set daily limit for an app is exceeded the watch vibrates with "You have been using <app> longer than you intended", dismissable only on the watch and repeating if use continues. In a two-week pilot (baseline week from phone history, one week watch face only, one week with alarms; n = 6 analysed), overall screen time fell significantly in the watch-face-only week but not in the alarm week, and use of limited apps fell 17% then only 6%. Participants liked the glanceable watch face and said the watch reduced phone unlocks by showing time and notifications, but found the alarms irritating and aggressive, set lenient limits or loosened them, and the effect faded as novelty wore off.

## Method

- Phone app (Kotlin, Jetpack Compose, Room): usage from UsageStatsManager (foreground app start/end, unlocks), dashboards mirroring Digital Wellbeing, per-app 24-hour clock view, weekly bars, health views from Google Fit (heart rate, steps, sleep).
- Watch app (Wear OS on a Suunto 7; Garmin rejected for weak phone–watch communication): WatchFace service with doughnut of top 5 apps + "other", total screen time, unlocks; list view; alarm screen. Phone–watch sync over the Wear OS data layer (Bluetooth, falling back to Wi-Fi/LTE via Google services), sending only changes to save battery; data stays on device unless exported.
- Alarm: triggered once a user-chosen limit is passed; if use continues, a vibration alarm after a 10 s threshold; same colour per app across phone and watch.
- Study: 9 bachelor students (bonus points) recruited by word of mouth, willing to detox; 3 at a time due to watches; baseline = 7 days before from phone history, passive week (watch face, no alarms), active week (alarms on apps they chose); survey after week 1; semi-structured interviews at the end. 3 excluded for incomplete data → n = 6 (5 men, mean age 23.5). Wilcoxon signed-rank tests.

## Results / evidence

- Overall screen time vs baseline: significant drop in the passive week (p = .031, effect size .57), not significant in the active week (p = .16).
- Apps with limits: −17% in the passive week (p = .029), −6% in the active week (p = .15).
- "Problematic" (endless-scroll) apps: about −5% between 19:00 and 07:00 in both phases; daytime use rose in the active phase.
- Alarms "did not perform as reliably as expected": described as exceedingly irritating; one participant avoided the app entirely to avoid the vibration; others set limits above their average or loosened them; one disabled Bluetooth, silently stopping alarms.
- Watch face well received as easier feedback than phone apps; the watch on the wrist acted as a constant reminder, but its effect faded.
- Participants reported unlocking the phone less because time and notifications were on the watch, though watch notifications can be just as distracting.
- Daily limits reset at midnight while heaviest problematic use was 22:00–01:00, so alarms often missed it.
- Health data: only sleep usable; heart rate and steps incomplete.
- Suggestions: snoozable alarms, progress toward the limit (e.g., hourly updates, colour coding), suggested limits from past usage, weekly goals.

## Strengths / limitations

- Strength: the only smartwatch intervention for digital well-being in my reading; full Android/Wear OS implementation described (APIs, sync, on-device data), with a passive vs active phase split.
- Strength: honest about failures (alarm aggression, lenient limits, midnight reset, Bluetooth off).
- Limitation: n = 6 of 9 students, no control group, one week per phase; with six pairs the smallest possible Wilcoxon p is .031, so the single "significant" result is at the floor.
- Limitation: the passive-week drop may be novelty, being observed, or end-of-semester workload (the authors note this); alarms only started in week 2, confounding order with intervention.
- Limitation: discussion overstates ("proved effective for most participants", "significant impact on phone usage") given the data; no battery measurements despite sync design for battery.

## How it relates to my thesis

Direct evidence for the smartwatch-as-companion idea raised in rosenberg2022: a watch can take over time-checking and notification triage, which may reduce phone unlocks (cf. cecchinato2017, bolle2015), and a glanceable watch face is a less intrusive form of feedback than phone dashboards. It also confirms what the intervention literature found on phones: a fixed vibration alarm after a limit irritates and fades (okeke2018), user-set limits drift lenient (kim2019goalkeeper), and effects drop after the first week (haliburton2024). Implementation details are reusable: UsageStatsManager for usage, Wear OS data layer for sync, on-device storage, and the lesson that "daily" limits should not reset at midnight. Its gaps (no control, n = 6, no battery data, two weeks) are exactly what a proper evaluation would need to address.

## Quotes / figures worth citing (with page)

- "digital devices and services are, at the same time, the source of the problem and the platform with which the interventions are delivered to the user." (quoting Monge Roffarello & De Russis, p. 84)
- "I would say that people tend to unlock their phone less if they have a watch just because you get notifications and you can check the time using the watch." (P1, p. 94)
- "In many instances, participants nearly unanimously characterized the alarms as exceedingly irritating and overly aggressive." (p. 95)
- "The mere presence of the smartwatch was found to be sufficient to prompt and remind participants to engage in a detoxification process." (p. 95)
- "In hindsight, resetting usage limits right before bedtime was counterproductive." (p. 95)
- Fig. 1, 6, 7: watch face and alarm (pp. 83, 91–92). Fig. 8: data flow phone–watch (p. 93). Fig. 10: usage by phase (p. 94). Table 2: study phases (p. 91).
