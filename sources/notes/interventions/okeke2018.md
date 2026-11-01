# okeke2018: Good Vibrations: Can a Digital Nudge Reduce Digital Overload?

**Authors / venue / year:** Okeke, Sobolev, Dell & Estrin / MobileHCI '18, Article 4 / 2018
**Link:** https://doi.org/10.1145/3229434.3229463 (code: https://github.com/fnokeke/FgApp)
**Relevance:** high

## Summary (3 sentences)

An Android app shows a low-priority status-bar notification with today's Facebook time and opens, and once a daily limit is exceeded it vibrates gently every 5 seconds while Facebook stays in the foreground, stopping as soon as the user leaves (nudge plus negative reinforcement, like a seat-belt chime). In a 3-week study (baseline, intervention, follow-up) with 50 Indian MTurk workers split into control, rigid limit (2 opens × 5 min) and personalised limit (50% of baseline), daily Facebook time fell by about 23% (8.5 min) in both vibration groups and not in the control. The number of opens did not change, the effect disappeared once vibration was removed, and most participants found the vibration irritating.

## Method

- App: Android only, because iOS gave no programmatic access to app usage. Persistent low-priority notification updated every 5 s with time and opens; vibration of two 100 ms pulses 100 ms apart, repeated every 5 s (5 s pause chosen from Pielot et al. to delay adaptation). Only foreground app use is monitored; Facebook in a browser is not.
- Design: 3 conditions, randomised; week 1 baseline (feedback only), week 2 intervention, week 3 follow-up (feedback only). All groups had the status-bar feedback.
- Limits set by researchers, not participants: rigid = 2 opens × 5 min/day (from an MTurk poll, median 30 min and 5 opens); personalised = half of the participant's baseline time and opens.
- Participants: recruited "Facebook habits" study on MTurk, no requirement to want to reduce use; restricted to India; Android users with the Facebook app already installed and ≥5 min/day. ~650 reached, 78 enrolled, 50 analysed (control 16, rigid 19, personalised 15). Paid $15.
- Analysis: within-condition Wilcoxon signed-rank tests (baseline vs treatment, baseline vs follow-up), Cohen's d; exit survey (n = 31); one-year follow-up survey (n = 21).

## Results / evidence

- Daily Facebook time, baseline → treatment: rigid −22.8% (d = 0.50, p = .009), personalised −23.3% (d = 0.60, p = .011), control no change (d = −0.08, p = .51); both −8.5 min/day.
- Follow-up week: no significant difference from baseline in any group; usage rose back after vibration stopped.
- Opens per day: no significant change in any group; the authors note vibration only starts after Facebook is already open and suggest a prompt at launch to target opens.
- Rigid vs personalised: no significant difference.
- Exit survey: 28/31 said the status-bar feedback increased awareness; participants pulled it down ~12 times/day. 26/31 found the vibration irritating (14 mildly, 12 very); 21 stopped using the app after a few minutes, 10 continued as normal; none quit Facebook.
- One year later (21 replied): 9 still felt they used Facebook too much, 19 said regulating app time is important, yet none used any regulating app.

## Strengths / limitations

- Strength: a single, isolated mechanism (vibration while over the limit) with a control group and a withdrawal week; open-source Android code; logged usage rather than self-report.
- Strength: recruits people who did not ask to reduce use, which is closer to a general population.
- Limitation: each phase lasts only one week, so no habituation curve and no lasting effect.
- Limitation: 36% of enrolled participants dropped and were excluded; groups of 15–19; Indian MTurk workers only; Facebook only.
- Limitation: the paper says it found "statistically significant differences between the three experimental conditions", but it only ran within-group tests; no between-group comparison is reported.
- Limitation: the exit survey reports vibration reactions for all 31 respondents, but 10 of them were controls who never received vibration, so those counts are unclear.
- Limitation: researcher-set limits (no user control); the rigid limit was chosen so most participants would be vibrated.
- Limitation: use on other devices or the browser is not captured.

## How it relates to my thesis

The most direct prior test of a vibration-based intervention on Android, and a model of an app small enough to build: a foreground-app check, a persistent notification and the Vibrator API, with code available. Its results set expectations: vibration cut time in the app but not opens, it irritated most people, and the effect vanished on withdrawal, consistent with haliburton2024 (friction works only while on) and the habituation and annoyance themes in almourad2021. The open-vs-time split connects to the checking-vs-screen-time distinction (cf. kim2019lockntype, which targets opens at unlock). It also leaves open what the authors list as future work: other nudges (screen dimming, LED, sounds), device-level rather than per-app triggers, and user-chosen limits (cf. kim2017pomodolock). The one-year follow-up, where nobody used a regulating app, matches parry2023's low adoption.

## Quotes / figures worth citing (with page)

- "the user's phone will issue gentle vibrations every five seconds, but the vibration stops once the user navigates away from Facebook." (Abstract, p. 4:1)
- "This suggests that applying digital nudges to curb technology overuse may not be sufficient in regulating mindless opening of mobile applications." (p. 4:7)
- "achieving long-term behavior change may require participants to experience negative reinforcement for an extended period of time (and perhaps indefinitely) or that the intervention should be applied during specific periods of time." (p. 4:8)
- "We focused on Android only because iOS does not provide programmatic access to monitor user applications." (footnote 1, p. 4:2)
- "negative reinforcement could apply to the entire device, such as alerting a user when they are excessively checking their phone or when it is unlocked for long periods of time." (p. 4:9)
- Table 1: effect sizes and p-values per condition (p. 4:6). Fig. 3–4: time on Facebook by period and % change (p. 4:7).
