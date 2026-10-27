# kim2019goalkeeper: GoalKeeper: Exploring Interaction Lockout Mechanisms for Regulating Smartphone Use

**Authors / venue / year:** Kim, Jung, Ko & Lee / Proceedings of the ACM on Interactive, Mobile, Wearable and Ubiquitous Technologies (IMWUT) 3(1), Article 16, 29 pp. / 2019
**Link:** https://doi.org/10.1145/3314403
**Relevance:** high

## Summary (3 sentences)

GoalKeeper is an Android app where users set a daily usage limit (as a commitment device) and the app reacts when they exceed it, in three intensities: a warning dialog (non-ILM), short escalating lockouts with 15-minute allowances (weak-ILM), or a full lockout until midnight (strong-ILM). In a 4-week counterbalanced field study (n = 36), stronger lockouts reduced usage more (weekday −32, −50 and −74 min/day vs baseline), but also raised frustration and coercion, and people set looser goals and changed them more often to avoid being locked out. Most preferred the weak lockout as a balance of pressure and freedom; the warning was ignored 92% of the time.

## Method

- Design tuned with 9 interviewees (lockout durations, allowance time, notification interval, one goal change per week).
- Goals: separate weekday/weekend daily limits set each Monday, with a recommended 10% or 20% cut from the baseline week; one modification allowed per week.
- Non-ILM: pop-up "You have exceeded your time limit goal… Will you continue using?" on unlock and every 15 min.
- Weak-ILM: lockouts of 1, 5, 15, 30, 60 min, each followed by 15 min of allowed use.
- Strong-ILM: phone locked (except dialer and contacts) until midnight.
- Common to all: usage timeline and stats, notification-bar status, warnings 30 and 5 min before the limit, user-triggered "break mode".
- 44 recruited (university portal, Android, transtheoretical stage 2–3: considering or ready to cut use), mean age 21.7, ~$45; 36 analysed (4 lost logs, 4 found workarounds). Week 1 baseline, then one week per condition in fully counterbalanced order. Weekly surveys (frustration from NASA-TLX, perceived coercion, focused immersion); exit survey and interviews.

## Results / evidence

- **Usage (weekdays vs baseline):** non-ILM −32.1 min (n.s.), weak −50.4 min (p = .008, d = 0.35), strong −73.7 min (p = .001, d = 0.54). Across conditions strong < non (p = .008). Weekends: all three reduced use, no difference between them.
- **Warnings ignored:** 92% chose "continue to use"; "It's only a dialog message. It does not lock my phone" (P32). Guilt faded with repetition.
- **Goal setting:** half based their goal on whether a lockout would follow (tighter goals with warnings, looser with lockouts); half just followed the recommendation. Goal increases: 5 participants under non-ILM, 15 under weak, 20 under strong, mostly for out-of-routine days (trips, navigation, visiting friends) and some for games/videos.
- **Self-report underestimates use** by ~30–36 min/day on average (baseline log vs survey).
- **Lockout awareness:** the risk of being locked out made people plan and ration use, check remaining time, keep the phone away; some saved time for urgent messages. Weak lockouts sometimes led to waiting it out or switching to a PC.
- **Frustration** (0–100): 36.2 non, 41.8 weak, 51.5 strong; **coercion** (1–5): 2.4 non → 3.9 strong.
- **Preference:** weak-ILM 52.8% ("well balanced between pressure and freedom"); strong-ILM least preferred but seen as useful for exam periods. More "addicted" participants (SAS) preferred the warning more often (41.7% vs 16.7%), although they might benefit most from stronger lockouts.
- **Break mode** helped concentration (mostly for study/work) but use halved over the weeks; people forgot or found it cumbersome.
- **Reset time matters:** a lockout late in the evening was fine, early in the day very frustrating; some waited until midnight to use the phone, which can hurt sleep.
- **Workarounds** via Android quirks (battery-saver stopping the timer, split-screen, returning from a call); once found, commitment collapsed.
- Design implications: guide goals (10–20% cut, capped), adapt lockout intensity over time and to the user's objective (e.g. exams), handle out-of-routine contexts (location-aware limits, whitelists), personalise reset time.

## Strengths / limitations

- Strength: logged usage, within-subject and fully counterbalanced; directly compares warning vs weak vs strong restriction.
- Strength: rich qualitative account of how people adapt to lockouts (planning, rationing, workarounds).
- Limitation: one week per condition, short exposure; small student sample; break mode present in all conditions may dilute effects.
- Limitation: outcome is screen time only, not checking frequency.
- Limitation: reporting errors: summary says 33.3% preferred strong and 13.9% the warning, but the text says the opposite; frustration ANOVA (F = 2.227, p = .023) and effect-size labels ("small" for η² = .54) don't fit; "graduate students" in the limitations vs a general university sample in the method; 3 vs 4 excluded for workarounds.

## How it relates to my thesis

Direct evidence on the effectiveness vs acceptability trade-off for any intervention: pure warnings get dismissed (like mongeroffarello2019's snoozed timers), strong lockouts work but frustrate and push users to loosen goals, and a light, temporary lockout is the preferred middle ground, which supports considering friction without full lock-out, in line with lyngs2019's point about delay. Useful design details: escalating short lockouts, allowance windows, warnings before the limit, capped goal changes, context exceptions, and caring about reset time. It also confirms self-report underestimates use, and that Android quirks (battery saver, split-screen) can break an intervention, which my technical evaluation should test. It cites Okeke et al. (Good Vibrations) as a "subtle, repeating phone vibration" nudge, a non-restrictive alternative closer to the vibration idea.

## Quotes / figures worth citing (with page)

- "restrictive mechanisms are more effective than non-restrictive mechanisms such as warning. However, we found that restrictive mechanisms caused more frustration and pressure to the users, mainly due to diversity of usage contexts and needs." (Abstract, p. 16:1)
- "Our data logs showed that 92% of the participants pressed the "continue to use" button (instead of the "quit" button) when the notification dialog appeared." (p. 16:18)
- "it is well balanced between pressure and freedom." (P20 on weak-ILM, p. 16:21)
- "This type of "anticipated punishment" acts as a proximal microboundary that provides continual friction with regard to the user interactions." (p. 16:24)
- "the stronger the ILM becomes, the more the need for flexibility increases." (p. 16:24)
- Fig. 8–9 (pp. 16:14–15): usage vs baseline and across conditions. Fig. 14 (p. 16:20): frustration and coercion. Fig. 15 (p. 16:22): preferences.
