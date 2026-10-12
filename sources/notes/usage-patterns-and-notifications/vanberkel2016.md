# vanberkel2016: A Systematic Assessment of Smartphone Usage Gaps

**Authors / venue / year:** van Berkel, Luo, Anagnostopoulos, Ferreira, Goncalves, Hosio & Kostakos / CHI '16, pp. 4711–4721 / 2016
**Link:** https://doi.org/10.1145/2858036.2858348 (author copy: https://nielsvanberkel.com/files/publications/chi2016a.pdf)
**Relevance:** medium–high (method for my logging)

## Summary (3 sentences)

Studies that log phone use merge sessions separated by a short screen-off gap (often 30 s, as in bohmer2011), but this threshold had never been tested. 17 Android users were asked at every unlock for a week whether they were continuing the previous objective or starting a new one; 67% of unlocks were new objectives, and even after gaps under 30 s about half (51%) were new. The best fixed threshold was 45 s, but it reached only 68% accuracy, and no classifier did better, so gap length alone cannot define a session.

## Method

- AWARE framework plugin on participants' own Android phones, 7 days. Logged screen on/off/lock/unlock, reboot/shutdown, battery, app launches, notifications.
- ESM popup on **every** unlock: "Why did you start using your phone?" → continue previous objective / start new objective. No other questions.
- N = 17 (13 M, 4 F, age 23–39, M = 26), university mailing lists; individual training session with examples of "objectives"; cinema ticket.
- Reviews the session definitions used in the literature (Table 1) and proposes a state model (locked vs unlocked sessions, app session vs phone usage session).
- Classifiers: constant threshold T (= current practice), "similar sets" (shared app categories between sessions), WEKA OneR (picked hour of day). 10-fold CV on 10 of 17 participants with enough data.

## Results / evidence

- 5,397 ESMs, 4,569 answered (83.8%); median answer time 2 s.
- 67.1% new objective, 32.9% continued; per person from 45% to 93% new.
- Mean gap before unlock: 15:26 min (continued) vs 35:06 min (new), but the distributions overlap heavily.
- Mean session: 2:46 min (new), 3:11 min (continued); one "use" (new + its continuations) 4:43 min.
- T = 30 s captures only 30.4% of true continuations; 50.85% of gaps < 30 s are followed by a new objective.
- Best T = 45 s → 68.0% accuracy (precision 70.6%, recall 95.6%); similar sets 64.2%; OneR 62.1%.
- Most continuations are a single extra session: objectives finish in 1–2 "visits".
- Notification → unlock within 2 min: 0.9% to 30.8% of notifications depending on the person; no link between reacting fast to notifications and the new/continued ratio (r = −.32, n.s.).
- Shows how much the definition matters: earlier work with T = 0 vs T = 30 s found 20 vs 13 sessions/day.

## Strengths / limitations

- Strength: first empirical test of session thresholds; ground truth from the user at every unlock; very high response rate.
- Strength: useful summary table of session definitions across studies.
- Limitation: 17 mostly male students/staff at one Finnish university, 1 week; classifier tested on only 10.
- Limitation: 68% accuracy is barely above simply calling every unlock "new" (67%), which the paper does not point out; the 45 s recommendation is weak.
- Limitation: asking at every unlock adds a step to every session and may change behaviour (participants said it did not).
- Limitation: locked-screen use (glancing at time or notifications) not covered; 7 participants had gaps in app data.
- Limitation: calls continuous gap/duration data "Poisson"; table numbering is inconsistent between text and tables.

## How it relates to my thesis

Directly relevant to how I define a "session" or a "pick-up" in my logs. It shows that a short screen-off gap usually starts a new objective, so every unlock is a meaningful unit, which supports counting pick-ups/unlocks (andrews2015, ellis2019) rather than merged sessions; if I merge, 45 s is the best-supported threshold, but I should report the choice and ideally show results for several thresholds. The wide range in notification → unlock rates (mostly < 15% within 2 min) agrees with heitmayer2021: most unlocks are not caused by a notification. Compare with bohmer2011 (30 s chains), andrews2015 (≤ 15 s checks), ferreira2014 (micro-usage ≤ 15 s) and oulasvirta2012 (≤ 30 s checks).

## Quotes / figures worth citing (page refs = author copy)

- "for the majority of instances where users return to their smartphone, i.e., unlock their device, they in fact begin a new session as opposed to continuing a previous one." (Abstract)
- "adopting a T=30 seconds threshold [...] actually only captures 30.37% of all true continuous sessions in our dataset. Additionally, our results show that 50.85% of gaps shorter than 30 seconds actually lead to a new session" (Discussion)
- "if a researcher insists on using a constant arbitrary threshold, we encourage fellow researchers to consider using a T=45 seconds threshold" (Discussion)
- Table 1: session definitions in the literature. Fig. 1: phone state model. Fig. 8: accuracy by threshold T.
