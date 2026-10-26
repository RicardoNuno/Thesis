# lyngs2019: Self-Control in Cyberspace: Applying Dual Systems Theory to a Review of Digital Self-Control Tools

**Authors / venue / year:** Lyngs, Lukoff, Slovak, Binns, Slack, Inzlicht, Van Kleek & Shadbolt / CHI '19, 18 pp. / 2019
**Link:** https://doi.org/10.1145/3290605.3300361 (preprint: https://arxiv.org/abs/1902.00157; data and code: https://osf.io/zyj4h)
**Relevance:** high

_Read from the arXiv preprint; quotes cite sections, not pages._

## Summary (3 sentences)

Reviews 367 apps and browser extensions for digital self-control (Google Play, Apple App Store, Chrome Web Store, Aug 2018) and codes their features into four clusters: block/removal, self-tracking, goal advancement, and reward/punishment. It maps these features onto a dual systems model of self-regulation: automatic System 1 habits vs conscious System 2 goals, with the strength of self-control set by the "expected value of control" (reward, expectancy, delay). Most tools block or remove distractions (preventing unwanted habits); few help build new habits or use delay, which the authors flag as the main gaps.

## Method

- Scraped store searches for "distraction", "addiction", "motivation", "self-control" (with "smartphone", "laptop", "internet" variants), US and UK stores → 4,890 tools → 731 relevant → 367 coded (86 Google Play, 58 App Store, 223 Chrome). iOS versions dropped when an Android version existed.
- Features coded from store descriptions, screenshots and videos; codebook built iteratively by three authors. A cluster counted as "core" if ≥ 25% of a tool's functionality.
- Also tabulated 17 HCI papers on self-control tools and the theories they used (Table 1): 7 used no theory, none used dual systems theory.

## Results / evidence

- **Block/removal (74%)**: blocking apps/sites (132), time limits (23), launch-count limits (3), launch delays (5); 50 tools add friction to override (non-stoppable sessions, passwords, effortful tasks, delays). Removing/hiding elements (139 tools, mostly Chrome): hiding newsfeeds, "reader" modes, minimal writing tools, minimal home screens.
- **Self-tracking (38%)**: usage history (105), visualisations (73), timers (72), tracking time *not* using the phone (42).
- **Goal advancement (35%)**: reminders of time/task goals (58) or values/quotes (52), explicit goal setting (58), comparing behaviour to goals (15).
- **Reward/punishment (22%)**: points/streaks (41), leaderboards/social sharing (27), achievements (21), virtual creatures like Forest's tree (20), real money or even electric shocks (10).
- 35% let the user choose what counts as a distraction (101 blacklists, 22 whitelists).
- 65% of tools focus on a single cluster; only Flipd and HabitLab cover all four.
- Store differences reflect developer permissions: browsers allow hiding UI elements; phones only allow blocking; iOS blocks even scheduled app blocking.
- Mapping to the model: 73% of tools prevent unwanted habits; only 18% scaffold new habits and 23% target delay (4% excluding timers).
- Research tools in Table 1 match the types in the field: tracking (Menthal, RescueTime, SAMS), hiding (Lottridge's tab dimming), blocking (AppDetox, PomodoLock, Freedom), goals + social sharing (NUGU), group muting (Lock n' LoL), night use (PreventDark), and **vibration nudges** (Okeke et al. 2018: pulsing vibration after a Facebook limit, stopping when the user leaves).
- Gaps: habit scaffolding (e.g. redirect from Reddit to Trello, location-triggered blocking), **delay** (only 2 tools slow app launches), expectancy/self-efficacy (encouragement after resisting an urge).
- Ego depletion explicitly rejected as an explanation (failed replications); the expected value of control is used instead.

## Strengths / limitations

- Strength: large, systematic store review with open data and code; clear taxonomy and a theory that explains *why* each feature should work.
- Strength: identifies concrete underexplored design spaces (delay, habit scaffolding, expectancy).
- Limitation: features coded from store descriptions, not from using the tools; no data on installs, reviews or effectiveness.
- Limitation: snapshot of 2018 stores; OS features (Digital Wellbeing, Screen Time) and newer apps not covered.
- Limitation: model is high-level, so mapping features to components involves judgement.

## How it relates to my thesis

Gives me the vocabulary and taxonomy for the State of the Art: the interventions I've seen (tracking, hiding, blocking, gamification / social sharing, awareness, muting, night-use limits) fit the four clusters, and the dual systems model explains them (blocking stops System 1 habits; tracking and goals support System 2). The gaps it names point to my design space: **delay** (slowing a check rather than blocking it), and scaffolding new habits instead of only preventing old ones, which also avoids the frustration of blocking (tran2019, cho2021). It also cites Okeke et al. 2018 (pulsing vibration after a usage limit), the closest existing work to my vibration idea, so I should read and cite it. The Android vs iOS permission point supports building on Android.

## Quotes / figures worth citing (with section)

- "the prevalence ranking was block/removal > self-tracking > goal advancement > reward/punishment." (Discussion)
- "The current landscape of digital self-control tools is dominated by features which prevent activation of unwanted non-conscious habits (73%)" (Results)
- "On mobile devices, however, developers have little control over how another app is displayed, leaving blocking or restricting access as the only viable strategies." (Results, store comparison)
- "only two of 367 reviewed tools directly focused on using delays to scaffold successful self-control" (Discussion, Delay)
- "context detection, a constant challenge in DBCI research for administering meaningful and well-timed interventions, is more manageable in relation to device use, because a large amount of relevant activity can be easily measured." (Discussion, Limitations and future work)
- Table 1: HCI tools and their theories. Fig. 1: dual systems model. Fig. 3: feature prevalence. Fig. 5–6: features mapped to model components.
