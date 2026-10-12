# ferreira2014: Contextual experience sampling of mobile application micro-usage

**Authors / venue / year:** Ferreira, Goncalves, Kostakos, Barkhuus & Dey / MobileHCI '14, pp. 91–100 / 2014
**Link:** https://doi.org/10.1145/2628363.2628367 (author copy: https://ubicomp.oulu.fi/files/mobilehci14.pdf)
**Relevance:** medium–high

## Summary (3 sentences)

Study 1 logged app sessions of 21 Android users for 3 weeks and found a natural break at ~15 s: 41.5% of app sessions ended within 15 s, which the authors call "micro-usage". Study 2 (15 new users, 2 weeks) popped up a short questionnaire after some micro-usages asking why, where and with whom: 62% were attributed to notifications, 18% to killing time, 11% to looking for something; most happened at home (53%) and alone (82%). Participants had never noticed this behaviour and explained it as "checking", which the authors link to oulasvirta2012's checking habit.

## Method

- AWARE logger on participants' own Android phones: app sessions via Accessibility Services (foreground app), screen on/off.
- Study 1: N = 21 (17 M, 4 F, age 22–40), 3 weeks, interviews before and after. 15 s threshold from Jenks natural breaks on session length.
- Study 2: N = 15 (9 M, 6 F, age 23–50), 2 weeks. ESM triggered when an app session lasted ≤ 15 s; max 10/day, ≥ 15 min apart (15 min = natural break in screen-off time), expires after 3 min. Questions: trigger (notification / killing time / accident / looking for something / other), location, social context. Real purpose of the study hidden until the end.
- Exit interviews with the 9 participants with > 40% micro-usage.

## Results / evidence

- Study 1: 41.5% of app sessions ≤ 15 s; 61% ≤ 30 s, 78% ≤ 4 min. Varies by app: Browser ~15%, Facebook 22.4%, Gmail 52.0%, Calendar ~60%.
- Study 2: 14,229 micro-uses detected; 762 ESMs, 642 answered (76%, ~3 per person per day). 36% of sessions ≤ 15 s (per person 19.7–66.3%).
- Most micro-used categories: email 40%, instant messaging 21%, SMS 16%.
- Triggers: notification 62%, killing time 18%, looking for something 11%, accident 6%.
- Location: home 53%; social: alone 82%. Notification-triggered micro-use mostly at home (52%), rarely at university (4%) or work (28%).
- No effect of age or gender on micro-usage.
- Screen-off time has a natural break at ~1,000 s (~15 min) between uses.
- Interviews: all 9 had never noticed their micro-usage; they explain it as "checking"; split views on notifications (5/9 essential, others a nuisance); 2 felt uneasy with no notifications.

## Strengths / limitations

- Strength: empirically derived threshold for a "check" instead of an arbitrary one; ESM asked in the moment, not recalled.
- Strength: separates system-initiated (notification) from user-initiated micro-use.
- Limitation: small samples (21 + 15), mostly male, one Finnish university town.
- Limitation: ESM only after short sessions, capped at 10/day and spaced 15 min apart, so the 642 answers are a selected sample of 14,229 micro-uses; and answering at home is easier (the authors admit this).
- Limitation: "home and alone" not compared with how much time people spend at home and alone, so it may just reflect where people are.
- Limitation: unit is the **app** session, not the phone session, so one pick-up with several quick app switches counts as several micro-uses.
- Limitation: Study 2 per-person mean is reported as 41.5%, identical to Study 1's overall figure; possibly a copy error.

## How it relates to my thesis

Defines and measures the "check" in logs: ≤ 15 s app sessions, the same cut-off andrews2015 used for checks (and below oulasvirta2012's 30 s). Gives the methods I can reuse on Android: AWARE / Accessibility foreground app, screen events, ESM triggered by short sessions. Tension with heitmayer2021: here 62% of micro-use is attributed to notifications vs 89% of pick-ups self-initiated there; the units differ (app sessions with an ESM vs every pick-up on camera), and once the phone is unlocked a notification may lead to a quick app open. Participants not noticing their own micro-usage fits andrews2015 and ellis2019 (people cannot estimate pick-ups). Their idea of pulling updates every ~15 min instead of pushing each one is a batching intervention worth noting.

## Quotes / figures worth citing (with page)

- "about approximately 40% of application launches last less than 15 seconds and happen most frequently when the user is at home and alone." (Abstract, p. 91)
- "participants attributed 62% of micro-usage instances to notifications" (p. 97)
- "All participants reported that they never recognized their micro-usage behavior before." (p. 96)
- "Participants repetitively used 'to check' their phones as an explanation for their micro-usage behavior, thus confirming our initial belief that the previously reported 'checking habit' [24] is often manifested as micro-usage." (p. 97)
- Fig. 1 (p. 93): session-length distribution with 15 s break. Fig. 2 (p. 93): micro-usage % by app. Fig. 6 (p. 95): triggers, location, social context.
