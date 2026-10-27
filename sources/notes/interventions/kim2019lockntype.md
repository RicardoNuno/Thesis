# kim2019lockntype: LocknType: Lockout Task Intervention for Discouraging Smartphone App Use

**Authors / venue / year:** Kim, Park, Lee, Ko & Lee / CHI '19, Paper 697, 12 pp. / 2019
**Link:** https://doi.org/10.1145/3290605.3300927
**Relevance:** high

## Summary (3 sentences)

LocknType is an Android app that, whenever a target app (browser, social media, entertainment) is opened, first shows a "lockout task": press OK (LT0), type 10 random digits (LT10) or type 30 digits (LT30), with the task picked at random. In a 3-week field study (n = 40), the task stopped the launch 13%, 27% and 48% of the time respectively, and launches of target apps halved compared to baseline. But total usage time didn't drop: sessions in target apps became about twice as long and use of other apps rose, so the friction mainly turned many short checks into fewer, longer sessions.

## Method

- Framing: expectancy-value theory (use if expected value > cost) and dual-process thinking; a lockout task adds cost and a "microboundary" that pushes from automatic (System 1) to reflective (System 2) use.
- Design dimensions: timing (just at app launch), mutability (users could not remove target apps, to stop workarounds), task type and workload (number entry, easy to quantify), scope (app level).
- Pilot (n = 10, 3 days): 10 vs 20 digits felt the same, so 20 was replaced by 0 (press OK); messaging and email removed after frustration and peer pressure to reply; workarounds found (deselecting apps, relaunching to get a shorter task), so deselection was disabled and the same task kept for 60 min.
- Main study: 40 Android users (18 F, mean age 23) wanting to cut use (transtheoretical stage 2–3), ~$40. Week 1 baseline logging; researchers then chose each person's target apps (~8.9) from their logs; weeks 2–3 lockout with LT0/LT10/LT30 at random. Interviews with 31 participants. 86,290 app launches and 26,272 lockout encounters logged.

## Results / evidence

- Task cost: LT0 1.9 s, LT10 7.2 s, LT30 17 s; first-try success LT10 77%, LT30 45%; NASA-TLX 12 / 20 / 31.
- Discourage rate (launch abandoned): LT0 13.1%, LT10 27.4%, LT30 47.5%; strong effect of workload (η² = .41), small effect of app category (browsers less discouraged).
- After abandoning: 25% turned the screen off (back to the task, talking to people, sleep), 50% opened a non-target app (mostly messaging), 24% tried another target app (often a browser to reach the same content).
- Overall usage vs baseline: target-app launches 0.51× (halved, p < .001), target-app time 0.92× (n.s.); non-target launches 1.25× and time 1.32× (both up); total launches and total time unchanged. Target-app session length rose from 84 s to 158 s.
- Even pressing OK made people pause: "Woah, what was I thinking? I don't need this right now." (P4).
- What drove use vs non-use: free time available, willingness/mindfulness, mood (used the phone anyway when feeling down), social norms (not typing in front of a partner), task urgency and importance, alternative apps or devices (switching between browsers to dodge the task).
- Design implications: light friction is enough for motivated users, others need more; use context to avoid blocking meaningful use; allow limited temporary exceptions; add guidance on what to do instead (as in MyTime).

## Strengths / limitations

- Strength: logged usage of all apps, so it shows where use went (displacement), not just whether the target app was used; large number of real encounters; graded friction levels in one study.
- Strength: directly tests delay/friction, the gap lyngs2019 identified (only 2 of 367 tools used delay).
- Limitation: no control group; baseline week vs intervention weeks only, 2 weeks of intervention.
- Limitation: researchers chose the target apps, not the users, and messaging was excluded; no measure of whether a blocked use was meaningful or not (false positives).
- Limitation: within-person random task levels, so effects of each level may bleed into each other.
- Limitation: inconsistent numbers: the introduction gives 12.9% / 26.5% / 46.2% discourage rates while the abstract and results give 13.1% / 27.4% / 47.5%; Table 1's confidence intervals don't contain the reported means.

## How it relates to my thesis

The key result is that friction at launch cut **checking** (launches halved) but not **time**, because people opened apps less often and stayed longer, or moved to other apps. That separates two goals an intervention could have: fewer impulsive checks versus less total use. The stopped launches show that even a confirm screen (press OK, ~2 s on average) makes many automatic checks reconsidered, which supports delay as a light alternative to blocking (lyngs2019, kim2019goalkeeper). The displacement to other apps and browsers is a warning for app-level interventions in general (cf. kim2017pomodolock's leak across devices). Technical points for Android: launch detection plus an overlay task, preventing users from removing targets, and handling workarounds like relaunching. Its suggestion to pair friction with guidance about what to do instead links to cho2021's "What were you going to do?" prompt.

## Quotes / figures worth citing (with page)

- "even the pause-only task that requires a user to press a button to proceed discouraged an average of 13.1% of app use, and the 30-digit-input task discouraged 47.5%." (Abstract, p. 1)
- "This implies that LT intervention only helped users to better manage interruptions or the frequent urge to use LT apps, by bundling frequent short sessions into less frequent long sessions." (p. 8)
- "At the moment when the 10 and 30 digit input task was shown, I was like, 'Woah, what was I thinking? I don't need this right now.'" (P4, p. 8)
- "Lockout tasks (as microboundaries between app use and non-use) gave the participants room to reconsider their app use intentions." (p. 9)
- Fig. 4 (p. 7): discourage rate per task. Table 1 (p. 8): usage change vs baseline for target and other apps. Table 2 (p. 9): determinants of use/non-use.
