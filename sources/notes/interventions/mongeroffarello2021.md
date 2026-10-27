# mongeroffarello2021: Understanding, Discovering, and Mitigating Habitual Smartphone Use in Young Adults

**Authors / venue / year:** Monge Roffarello & De Russis / ACM Transactions on Interactive Intelligent Systems 11(2), Article 13, 34 pp. / 2021
**Link:** https://doi.org/10.1145/3447991 (author copy: https://iris.polito.it/bitstream/11583/2867117/1/habitsdetection.pdf; source code: https://git.elite.polito.it/public-projects/socialize-v2)
**Relevance:** high

## Summary (3 sentences)

Defines a smartphone habit as a recurring link between a context cue (time slot, workday/holiday, location, physical activity, a just-received notification, or a previous app) and the apps used in a phone session, and mines these automatically from logs with clustering (DBSCAN) and association rules (Apriori). Tested on 137,230 sessions from 35 young adults: habits were highly individual, users recognised them as their own, and the more negatively they saw a habit the more they wanted to avoid it. Built into a new version of Socialize (Android), which notifies a detected habit in real time, lets the user mark it as meaningless, asks why they do it and what they'd rather do, then shows that intention as a just-in-time reminder whenever the habit recurs; in 20 users this cut time on flagged habits from 77 to 48 s per occurrence.

## Method

- Literature review (30 papers) coded into what habits are (checking, revisitation…), why they form (cue + reward: intrapersonal, contextual; informational, social), when they can be predicted (notifications, next app, mood, usage classes).
- Session = screen on to screen off; each session as a "bag of apps" weighted by time (TF-IDF); clustered with DBSCAN (cosine similarity, silhouette check); then each cluster's sessions combined with context and mined with Apriori (lift > 1, support > 1%).
- Context: 2-hour time slots, workday/holiday, Google Activity Recognition (still, walking, running, cycling, vehicle), home/work geofences, preceding notification.
- Three habit types: Context habits (context → apps, e.g. {workday, 10–12, work} → {Facebook, Instagram}), App habits (app → apps, e.g. WhatsApp → Twitter, Facebook), App-Context habits.
- Interviews (n = 10): rated 10 of their own mined habits for familiarity, habitualness, positivity and wish to avoid.
- Socialize v2 (on-device, simplified: no clustering, rules recomputed daily over last 7 days, productivity/tools apps excluded): habit notification → "Avoid habit" → choose motivation (bored, lonely, need to communicate, sad/nervous, fun, or own) → write an alternative intention → reminder each time the habit is detected.
- Field study: 67 installed, 20 analysed (19–31, all students); week 1 silent logging, then intervention; 21–113 days of use; metrics: time on the flagged habit, and total phone time in that context (to check for displacement); Wilcoxon tests on first 21 days.

## Results / evidence

- Mining: ~3,845 sessions/user, 83% clustered, ~10 clusters per user (range 4–22); most common clusters were messaging + social (Facebook, Instagram, WhatsApp).
- Interviews: habits familiar (5.3/7) and habitual (5.2/7), seen as mostly negative (3.2/7), wish to avoid 4.8/7; less positive → more wish to avoid (r = −.83). Context-triggered habits were the most disliked; app-only habits the least recognised. "Being alerted when one falls into the trap of some specific habits would be very useful" (U6).
- Field: 94 habit notifications; 40 (43%) turned into reminders, 17 of 20 users activated at least one; 80% of reminders still active at analysis.
- Flagged habits: 60% on workdays, 75% while still (desk, class); 60% social, 40% messaging, 15% web/video. Motivations: bored 60%, lonely 15%, sad/nervous 10%. Intentions: study/work 40%, a specific activity (sleep, read, walk) 35%.
- Effect: time on flagged habit 76.8 → 48.2 s (p = .004); 70% of reminders "successful"; total phone time in the same context 313 → 202 s (n.s. overall, significant for successful reminders), i.e. little displacement to other apps.
- Worked for social apps (96 → 52 s, p = .025), not for messaging (39 → 33 s): reminders help with passive use, not with communication.
- Some effect remained after users disabled reminders (36 → 23 s, n.s.).
- Users didn't feel their use had changed (2.5/5) and said notifications are easy to ignore, although logs showed a reduction.

## Strengths / limitations

- Strength: a concrete, open-source pipeline from Android logs to personalised habit detection to a timed intervention; habits defined by context, not only by app.
- Strength: user decides which habits are meaningless; reminders use the user's own alternative ("go for a walk") rather than a prohibition.
- Strength: checks displacement (time in the same context on any app).
- Limitation: no control group; pre/post only; 21-day analysis window.
- Limitation: 67 → 20 users after excluding those with too little data or missing GPS/location, a strong filter that may keep only the most engaged.
- Limitation: small effects in absolute terms (seconds per occurrence); students only.
- Limitation: location tracking (GPS) needed for context habits, which is privacy-heavy and failed for many users.

## How it relates to my thesis

The closest example of a full technical pipeline of the kind my proposal describes: Android logging of screen, app, notification, activity and location events, automatic detection of patterns, and an intervention delivered at the moment the pattern occurs, evaluated in the field. It is a concrete AI/adaptive approach (association-rule mining rather than a black-box model, so its output is readable and the user can confirm or reject each habit, which matches anderson2018's call for transparency). It operationalises ideas from other papers: tran2019's triggers become context cues, cho2021's regret becomes user-flagged meaningless habits, hiniker2016's aspirations become the user's own alternative intention, and lyngs2019's gap on habit formation is addressed by encouraging a replacement behaviour. It also answers mongeroffarello2019's finding (time down, checking unchanged) by targeting the habit itself. Technical lessons: Google Activity Recognition and geofencing for context, rules recomputed daily on-device, and losing many users to location permissions.

## Quotes / figures worth citing (with page)

- "Behavioral routines triggered by precise contextual cues, for example, are more likely to be considered negative and meaningless behaviors, and the less a habit is positively perceived, the more the user would like to change it." (p. 13:3)
- "this digital wellbeing tool is the first example of a mobile app that monitors and notifies smartphone habitual behaviors in real-time." (p. 13:28)
- "just-in-time reminders are effective with apps that are mainly used passively, e.g., social media, while they have little impact on the use of communication apps." (p. 13:26)
- "we did not include a control group. Therefore, we must acknowledge that some reduction effects of Socialize may have been circumstantial." (p. 13:29)
- Fig. 3 (p. 13:10): habit-discovery pipeline. Table 4 (p. 13:15): habit types. Fig. 8 (p. 13:20): Socialize flow. Table 10 (p. 13:24): effect on flagged habits.
