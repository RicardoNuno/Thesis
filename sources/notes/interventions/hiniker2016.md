# hiniker2016: MyTime: Designing and Evaluating an Intervention for Smartphone Non-Use

**Authors / venue / year:** Hiniker, Hong, Kohno & Kientz / CHI '16, 4746–4757 / 2016
**Link:** https://doi.org/10.1145/2858036.2858403 (author copy: https://homes.cs.washington.edu/~yoshi/papers/MyTimeCameraReady.pdf)
**Relevance:** high

_Skimmed from the camera-ready author copy, which has no page numbers; quotes cite sections._

## Summary (3 sentences)

A designer brainstorm (100 ideas) was clustered into eight intervention categories, and a survey of 232 people rated one mockup per category; the three most wanted (a usage timer, a daily time-limit "Time's up!" dialog, and a daily "aspiration" prompt) were built into MyTime, an Android app where users pick the apps they want to monitor. In a deployment with 23 users (one baseline week, one week with MyTime), total phone use fell by 33 min/day (11%), and specifically use of apps users considered a waste of time fell by 21%, while monitored apps they valued didn't change. What people want to change predicted which features they wanted and what worked for them: people wanting to cut use responded to limits, and people wanting context-specific change used the aspiration prompt, which made them more likely to leave the app.

## Method

- Design taxonomy from a brainstorm with five designers: **information, reward, punishment, disruption, limit, mindfulness, appeal to values, social support** (Table 1). One mockup per category (timer, charity donation, phobia images, icon scramble, timeout, aspiration, watermark of what matters to you, sharing progress with supporters).
- Survey: 232 US Mechanical Turk workers ("interested in reducing or changing phone use"), $2; rated and ranked the mockups; open answers coded (e.g. "If you could change one thing about the way you use your phone…").
- MyTime (Android): user selects "monitored" apps and a daily limit; background service logs foreground app use. **Timer:** persistent notification with time on current app and on all monitored apps vs the limit. **Timeout:** at the limit a "Time's up!" dialog with "I need a few more minutes" (time picker) or "Exit [app]"; dismissing brings it back every 5 min or 10% of the limit. **Aspiration:** daily prompt "What is one thing you would like to accomplish today?", reflected back in the timeout dialog as "Try this instead: …".
- Deployment: 23 Android users across the US (19 women, mean age 33.5), $45; one week silent baseline, then one week with all features.

## Results / evidence

- Survey: 74% wanted to use the phone less (58% a little, 16% much); most common wish was to limit a specific activity (33%), mostly social media (37%) and games (30%); Facebook named as draining 70 times.
- 79% "reduction-focused" (want to cut something), 12% "context-focused" (e.g. not before bed, not around people).
- Preferred mockups: timer, aspiration and timeout; neutral on watermark and charity; disliked scramble, phobia and social sharing. People liked awareness, reminders of priorities and enforcement; disliked features that spoil the app, reduce control, are painful, lack enforcement, or that they'd get used to.
- Deployment: total use −33 min/day (11%, η² = .056); monitored apps −23 min (−18%); apps users had called a waste of time −24 min (−21%); valued monitored apps unchanged.
- Users monitored valued apps too (59% tracked at least one app they considered a good use of time); 116 different apps, Facebook by ~90%.
- "Time's up!" shown 370 times: dismissed 64%, extension requested 30% (median 15 min, most often 1 min), exited 6%. More likely to exit social media apps; more extensions for valued apps; reduction-focused users exited more and cut more.
- Aspirations: half the users never set one, the other half ~5 a week; seeing their own aspiration in the dialog made users more likely to exit the app; context-focused users set more.

## Strengths / limitations

- Strength: goes from design space (8 categories) through user preferences to a deployed, logged app; separates valued from unwanted use instead of treating all use as bad ("targeted non-use").
- Strength: links what users want to change to which intervention type works for them.
- Limitation: only **one week** of intervention after one baseline week, no control group; novelty effects likely.
- Limitation: 23 participants, mostly women; survey on Mechanical Turk with recruitment aimed at people wanting to reduce use.
- Limitation: "waste of time" vs "good use" is per app, not per use; apps not mentioned were grouped with "waste of time".
- Limitation: Android-only foreground-app tracking; warnings mostly dismissed, so the effect may come from awareness (timer) more than the timeout.

## How it relates to my thesis

A classic baseline for a non-blocking Android intervention: a usage timer, a soft limit and a goal reminder cut unwanted use by about a fifth in a week without touching valued use. Its eight-category taxonomy complements lyngs2019's four clusters, and its "disruption" category is the space LocknType and the vibration idea fall into. The aspiration feature ("What is one thing you would like to accomplish today?" shown again at the limit) is evidence for reminding people of their own goals at the moment of use, the same idea as cho2021's "What were you going to do after this?" and LocknType's call for guidance on what to do instead. The fact that the dialog was dismissed 64% of the time echoes kim2019goalkeeper's ignored warnings. Also shows users want to monitor *some* apps for information only, so an intervention should let them separate "track" from "limit". Same short-exposure limitation as most studies here.

## Quotes / figures worth citing (with section)

- "participants reduced their time with the apps they feel are a poor use of time by 21% while their use of the apps they feel are a good use of time remained unchanged." (Abstract)
- "interventions to support non-use can preserve the value users reap from technology while surgically targeting experiences that users find to be a poor investment of their time." (Discussion)
- "Seeing a self-defined aspiration about phone use or a suggested alternative left participants significantly more likely to quit the app they had been using." (Deployment Results, Aspiration Feature)
- "We do not know how the behavior change catalyzed by MyTime fares in the long term" (Limitations and Future Work)
- Table 1: eight intervention categories. Table 3: what users want to change. Fig. 3: MyTime features. Fig. 5: use of valued vs wasteful apps.
