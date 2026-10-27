# mongeroffarello2019: The Race Towards Digital Wellbeing: Issues and Opportunities

**Authors / venue / year:** Monge Roffarello & De Russis / CHI '19, Paper 386, 14 pp. / 2019
**Link:** https://doi.org/10.1145/3290605.3300616 (author copy: https://iris.polito.it/bitstream/11583/2724317/1/digitalwellbeing.pdf)
**Relevance:** high

## Summary (3 sentences)

Three studies on commercial digital wellbeing apps: a feature review of the 42 most popular Android apps, a thematic analysis of 1,128 Play Store reviews, and a 3-week field study of Socialize, an Android app the authors built with the most common features, with 38 participants. The apps are liked and help in specific cases (Socialize cut daily usage time and social-network time), but they did not change how often people checked their phones: unlocks, app launches and compulsive checking stayed the same, and timers/blockers were mostly snoozed or deleted. The apps rely on self-monitoring and breaking habits, not on forming new ones or social support, and users say they are too easy to bypass.

## Method

- **Feature review:** Google Play search (July 2018: "digital diet", "smartphone addiction", "avoid distractions", "screen time", "app/phone usage tracker"); ≥ 1,000 downloads and ≥ 50 reviews → 42 apps, 19 features. Android only because iOS doesn't expose usage statistics.
- **Reviews:** first 50 "most helpful" reviews per app → 1,128 English reviews (2015–2018, mean 3.79/5); hybrid thematic coding (κ = 0.95).
- **Socialize:** Android app with every feature in ≥ 15% of apps: phone/app usage time, unlocks, app checks, notifications; dashboard, hourly charts, persistent notification recap; phone/app timers, blockers, "take a break"; optional context (activity, location). On trigger a pop-up lets the user respect, snooze or delete the intervention. Notification blocking left out because the Android SDK doesn't allow it.
- **Field study:** 69 installed, 38 completed (24 M; mean age 22.5; mostly students), July 2018. Week 1 silent logging (baseline), weeks 2–3 full app. SAS-SV and an adapted self-efficacy (GSE) scale before and after; exit survey.

## Results / evidence

- **Features (42 apps):** charts 60%, phone summary 57% (phone time 52%, unlocks 27%), app summary 50% (app time 48%, app checks 15%), daily/widget recap 38%, app timers 31%, app blockers 26%, phone timers 26%, notification blockers 19%, phone blockers 15%, take a break 15%, social comparison 14%, quotes 12%, rewards 10%; automatic interventions and UI redesign (e.g. shuffling addictive app icons) only 2% each.
- **Reviews:** 55% positive, 37% negative. Liked: statistics (9%), timers/blockers (5%), awareness ("the inconvenient truth"), impulse control, focus, use for studying, work, sleep, parental control. Disliked: bugs (29%), especially inaccurate tracking (19%, e.g. background time counted as use); easy to bypass (7%: "I can just simply uninstall this app"); some users hand the password to a partner or offer root access to make it stricter; a few privacy complaints.
- **Socialize usage (baseline → intervention):** daily usage 234 → 197 min (significant); used apps 23.9 → 22.4 (significant); unlocks 122 → 117 and app launches 631 → 582 (n.s.); compulsive checks (sessions < 1 min apart) 49.7 → 52.5 (n.s.); social-network time down (38 → 33 min), messaging unchanged; SAS-SV and self-efficacy unchanged.
- **Interventions:** only 41 set (6 phone timers, 11 app timers, 7 phone blockers, 16 app blockers, 1 break); 2/3 at app level, mostly for Facebook and Instagram. Phone timers triggered 91 times, respected twice (snoozed 97.8%); app blockers triggered 245 times, respected 115; all blockers deleted before the end; the one break was ignored. Context customisation rarely used (9 of 40).
- All 38 said they would keep using it; many were shocked by their own statistics; 3 complained about battery.
- Design recommendations: ground apps in habit formation (cues, triggers, positive reinforcement, suggest replacement habits), add social support (comparison, social games), make interventions harder to bypass with penalties, focus on app level, and make statistics accurate and explainable.

## Strengths / limitations

- Strength: combines a market review, real user voices and logged field data; Android implementation close to what I plan to build.
- Strength: logged unlocks and compulsive checks, not just screen time, which exposes that time dropped but checking didn't.
- Limitation: 3 weeks, 38 mostly student participants, overlapping with exams; no control group (pre–post only), so the drop in time may be novelty or seasonal.
- Limitation: within-subject data analysed with independent t-tests (should be paired / repeated measures); some numbers don't add up (130 of 245 snoozes reported as 54.06%; blockers "deleted before the end of the collection phase").
- Limitation: reviews are biased to extreme opinions; "users want restrictive tools" rests on only 11 reviews plus snooze behaviour.
- Limitation: 2018 apps, before Android's built-in Digital Wellbeing was widespread.

## How it relates to my thesis

The closest predecessor to my prototype: an Android app with the standard wellbeing features, evaluated in the field, that reduced screen time but **not checking**. That is exactly the gap my thesis targets, and it supports measuring unlocks and compulsive checks, not only minutes. Its feature table is a ready baseline for comparing my design against commercial apps and Digital Wellbeing (the proposal's baseline). It also documents Android limits (no notification control from the SDK, tracking accuracy, background time counted as use, battery complaints), which matter for my technical evaluation. Its conclusion that users want *stricter* tools conflicts with tran2019, kim2017pomodolock and mark2018 (restriction frustrates or must stay under user control); a sensible reading is that easily snoozed timers are ignored, so an intervention needs some friction without becoming a lock-out (cf. the delay gap in lyngs2019).

## Quotes / figures worth citing (with page)

- "contemporary digital wellbeing apps are mainly focused on supporting self-monitoring, i.e., tracking user's behavior and receiving feedback, but are not grounded in habit formation nor social support literature." (p. 2)
- "even by using Socialize, participants continued to constantly check their smartphones." (p. 9)
- "contemporary digital wellbeing apps are mainly designed to break existing habits, instead of developing new habits. Breaking habits, however, is frustrating" (p. 11)
- "Perhaps the most interesting result of our work is that users want restrictive solutions to limit their excessive smartphone use." (p. 12)
- Table 1 and Fig. 1 (p. 3–4): features of 42 apps. Table 4 (p. 8): usage metrics before/after. Table 5 (p. 9): interventions set, triggered, respected, snoozed.
