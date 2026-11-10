# visuri2021: Understanding usage style transformation during long-term smartwatch use

**Authors / venue / year:** Visuri, van Berkel, Goncalves, Rawassizadeh, Ferreira & Kostakos / Personal and Ubiquitous Computing 25(3), 535–549 / 2021
**Link:** https://doi.org/10.1007/s00779-020-01511-2 (open access)
**Relevance:** low

## Summary (3 sentences)

Logging data from 79 anonymous Android Wear users (Insight4Wear app, Dec 2015 – Mar 2017, 4–14 months each) were turned into 98 features about notifications, screen sessions, battery and day-to-day use, summarised per 30-day window and clustered into 33 usage behaviours. Behaviours whose popularity rose over time were labelled "accepted" and those that faded "exploratory"; users showed about three behaviours each, rarely went back to an earlier one, and often stayed in the same one for months. Accepted, long-term behaviours were more passive: about 65 fewer notifications a day, fewer notifications observed promptly, fewer notification-initiated sessions, about 26 fewer sessions a day, shorter usage streaks, and more frequent charging, which the authors read as users learning not to be constantly available through the watch.

## Method

- 81 users with ≥ 120 days of data (2 removed as outliers → 79); no demographics (US 33%, UK 13%, Central Europe 13% of installs).
- Features (98): notification counts and category ratios, share observed within 60 s, reward-based (SIRB) use, session counts/lengths, short/isolated sessions, glance (exactly 5 s) sessions, hourly session and charging probabilities, battery drain and charge levels, streaks/breaks/phases; noisy apps (e.g., GPS status) filtered.
- 468 30-day summaries, z-scored; k-means with k chosen by Dunn index and entropy (k = 33); trends in each cluster's popularity over months via Pearson correlation; accepted vs exploratory compared with t-tests/KS tests.

## Results / evidence

- Users showed 3.4 behaviours on average (2–6); 56.7% of transitions were no change; returns to a previous behaviour 20.1%.
- 16 behaviours rose in popularity ("accepted"), 10 fell ("exploratory"); only one rising trend was significant at p < .01.
- Accepted vs exploratory: −64.8 notifications/day, −0.30 in share of promptly observed notifications, −0.03 in notification-initiated sessions, −25.6 sessions/day, shorter usage streaks (−2.7 days) and phases (−3.7 days); more evening charging and frequent top-ups.
- Glance-session share (time checks) did not differ.
- Authors' design points: watches should manage which notifications are shown automatically and offer easier controls than per-app settings (Android O notification channels a step forward); a minimal "essential mode" design (e.g., TicWatch Pro's dual screen) may fit long-term use better than a full phone sidekick.

## Strengths / limitations

- Strength: long-term, in-the-wild logging (up to 14 months) of real owners rather than study-issued devices.
- Limitation: "accepted" vs "exploratory" rests on popularity trends that were mostly not significant; "accepted" could equally reflect disengagement as contentment, and no user reasons were collected.
- Limitation: anonymous self-selected users who installed a logging app, starting at different points in ownership; old Android Wear devices; no phone data.
- Limitation: reporting slips: "Games" listed as increasing with a negative difference, a "p < −0.05", and 56.7% used for two different statistics.

## How it relates to my thesis

Shows that over months watch owners drift toward fewer notifications and less constant availability, consistent with cecchinato2017's interviewees turning off watch notifications after the novelty wears off. For a watch companion that means the useful long-term role is a filtered, low-interruption channel rather than a mirror of the phone, and that engagement with any watch feature naturally declines after the first weeks (cf. shahu2024's fading effect). It says nothing about whether this reduces phone use.

## Quotes / figures worth citing (with page)

- "In general, the accepted smartwatch usage behaviour tends to be more passive." (p. 542)
- "there is no need to constantly rely on the smartwatch or being connected." (p. 545)
- "efforts should be made to (i) automatically manage the notifications shown through the smartwatch and (ii) offer the user more effortless tools in managing notifications." (p. 545)
- "the smartwatch as a completely functional sidekick for the smartphone might not necessarily be the optimal nor desired design." (p. 546)
- Fig. 1: analysis pipeline (p. 538); Table 1: features (p. 539); Fig. 3: notification differences (p. 543); Table 2: assumptions validated (p. 546).
