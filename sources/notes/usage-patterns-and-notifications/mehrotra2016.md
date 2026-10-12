# mehrotra2016: My Phone and Me: Understanding People's Receptivity to Mobile Notifications

**Authors / venue / year:** Mehrotra, Pejovic, Vermeulen, Hendley & Musolesi / CHI '16, pp. 1021–1032 / 2016
**Link:** https://doi.org/10.1145/2858036.2858566 (accepted version: https://discovery.ucl.ac.uk/id/eprint/1502364/)
**Relevance:** medium

## Summary (3 sentences)

An Android app logged every notification (arrival, seen = next unlock, clicked or dismissed) and asked about 4 of them per day: why it was handled that way, what the user was doing, how complex the task was, and how disruptive it felt. 20 users (10,372 notifications, 474 questionnaires) saw notifications fastest on vibrate and slowest on silent, yet missed fewer alerts on silent than on sound; perceived disruption rose with task complexity and mid-task timing and was lowest when idle. More disruptive notifications were more likely to be dismissed, but 54% of the disruptive ones were still clicked because the content was important or useful.

## Method

- "My Phone and Me" on Google Play (Aug 2015), no payment; NotificationListenerService for notifications, unlock events for "seen". App also showed users their own usage stats.
- 74 installed, ~2 months; analysis limited to 20 users with ≥ 14 questionnaires (11 M, 9 F, age 19–50). 11 completed a Big Five test (IPIP 50 items).
- ESM: one random handled notification per 4 h window 8:00–20:00, plus one 20:00–22:00; questionnaire shows a screenshot of the notification. 9 questions (alert noticed, how handled, reasons, sender relationship, task, completion level, complexity, disruption).
- Seen time = arrival → next unlock (0 if already using the phone); decision time = seen → click/dismiss. ANOVAs, Spearman/Kendall correlations, logistic and linear regression.

## Results / evidence

- Ringer mode at arrival: 25.5% silent, 21.5% vibrate, 41.9% sound, 11.0% sound+vibrate. Missed alerts: 14.6% silent, 15.4% vibrate, 23.8% sound, 21.1% sound+vibrate (self-reported).
- Mean seen time: silent 7.3 min, sound 5.95 min, sound+vibrate 4.8 min, vibrate 3.35 min (n = 4,929).
- Seen time fastest while communicating (47 s), slowest when idle (9.5 min); more complex task → faster seen (ρ = −.18).
- Decision time depends only on sender: partner 3.3 s, close family 4.9 s, extended family 11.9 s.
- While using the phone: high-priority (heads-up) notifications answered in 11.9 s vs 25.9 s for low-priority ones (shade only).
- Disruption: task complexity τ = .48; highest during work, lowest when idle; highest mid-task or finishing, lowest when idle or starting; highest from "not a person" (system/app) and subordinates.
- Each +1 point of disruption → odds of accepting × 0.58 (R² = .14).
- 104/474 notifications rated disruptive; 54% of those still clicked (reasons: content useful 35%, important 33%).
- Overall click rate 62.5%; top reasons to click: "I was free" 37%, sender important 32%, content useful 32%.
- Personality (N = 11): extroversion → more disruption (R² = .74); extroversion, conscientiousness and neuroticism → seen time (R² = .90).

## Strengths / limitations

- Strength: real notifications from the user's own apps, with a screenshot shown in the questionnaire to cut recall bias.
- Strength: splits response into "seen" and "decision" time.
- Limitation: 20 of 74 users kept (the most compliant ones); questionnaire notifications were clicked more (70%) than average (62.5%).
- Limitation: "seen" = next unlock, so glances at the lock screen and notifications seen while already using the phone (seen = 0) distort the timing.
- Limitation: repeated answers from the same users treated as independent in ANOVAs (the authors admit this).
- Limitation: personality regressions with 5 predictors on 11 people (df = 5): the high R² values are almost certainly overfitting.
- Limitation: the app showed usage stats ("tells the users about their addiction"), which may itself change behaviour.

## How it relates to my thesis

Supports pielot2014: silent mode does not stop people noticing notifications and only delays viewing by a few minutes. Gives a ready logging design for Android (NotificationListenerService + unlock events, seen vs decision time). People knowingly accept disruption when the content is valuable, so blocking notifications outright is not what users want; deferring them until the user is idle or starting a task fits better (their own implication). Because seen time is measured as the next unlock, a notification can only be "seen" at a pick-up, which is the same event heitmayer2021 shows is mostly self-initiated; logs alone cannot tell whether the notification caused the pick-up. Idle moments: slowest to see but least disrupted, consistent with boredom-driven checking (heitmayer2021).

## Quotes / figures worth citing (page refs = accepted version, sections)

- "We found that even a notification that contains important or useful content can cause disruption." (Abstract)
- "setting the phone to silent does not help in escaping interruptions." (Understanding Response Time)
- "the likelihood of the acceptance of a notification decreases by 0.581 times [...] for a unit increase in the perceived disruption" (Understanding the Acceptance of Notifications)
- "54% of these disruptive notifications were accepted (clicked) by the users, regardless of the fact that they caused disruption." (Why are disruptive notifications accepted?)
- Fig. 2: seen time vs decision time. Table 2: ESM questions. Tables 3–5: reasons for clicking/dismissing.
