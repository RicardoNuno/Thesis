# haliburton2024: A Longitudinal In-the-Wild Investigation of Design Frictions to Prevent Smartphone Overuse

**Authors / venue / year:** Haliburton, Grüning, Riedel, Schmidt & Terzimehić / CHI '24, 16 pp. / 2024
**Link:** https://doi.org/10.1145/3613904.3642370 (author copy: https://www.medien.ifi.lmu.de/pubdb/publications/pub/haliburton2024chi/haliburton2024chi.pdf; data and scripts: https://github.com/mimuc/one-sec)
**Relevance:** high

_Skimmed from the LMU author copy; quotes cite sections._

## Summary (3 sentences)

Analyses historical logs from 1,039 existing users of the commercial app one sec, which, when a user opens an app they've chosen to target, shows a short friction (by default a 6-second breathing animation) and then asks whether to continue or close. Over 13.4 weeks on average, attempts to open target apps dropped steeply in the first ~3 weeks and then levelled off, while the share of attempts users dismissed also fell, i.e. fewer but more intentional openings; over 80% of targeted opens were social media, mostly Instagram. A quarter of users took breaks (often Friday to Sunday): use rose sharply just before a break and was high on return but dropped again within hours, suggesting the friction works only while it is active.

## Method

- one sec (iOS/Android): when a target app is opened, a friction of 3–60 s (default 6 s) with an animation (breathing exercise, follow a dot, rotate phone, mirror/selfie, black screen), then "continue" or "dismiss". Users choose target apps, type and duration; optional incremental durations and schedules.
- Recruitment via an in-app banner (Dec 2022–Apr 2023); 1,039 users donated historical logs (1.3M interventions); 249 answered an optional open-ended survey (mean age 25.8, 60% male).
- Logged per intervention: anonymous ID, target app, continue/dismiss, timestamp, friction type and duration. No data before installation and none for non-target apps.
- Analysis: Mann-Kendall trends and exponential vs linear fits over time; breaks defined as gaps > 2 SD (≈ 48 h); hourly patterns around first use and breaks; day-of-week mixed models; top-down qualitative coding.

## Results / evidence

- Targets: 81% of open attempts were social media, Instagram 38%; every user targeted at least one social app; users targeted ~3.7 apps.
- Setup: 90% used the default 6-s breathing exercise; most kept defaults (mean friction 7.8 s); "Rotate phone" least used (noticeable in public).
- Overall users continued 67% and dismissed 33% of attempts.
- Over time: open attempts per user per day fell exponentially, flattening after ~20 days; the dismissal rate also fell, so later opens were more deliberate. "Now, I usually continue to the app but it's because when I click on it I tend to have an objective." (P43)
- Some got used to it: "my brain has gotten used to the waiting before an app opens" (P162).
- Breaks: 27% of users took at least one (mean 9 days, most often ~2 days); more likely to start on Friday and end on Sunday; use spiked right before a break and on return, then dropped back within hours.
- Users wanted to split parts of an app (e.g. Instagram messages vs feed); other tools (Screen Time limits, deleting apps) were too easy to bypass or too drastic.
- Authors suggest ~3 weeks is enough to see the main behavioural effect in intervention studies.

## Strengths / limitations

- Strength: large, organic, long-term data (mean 13 weeks, up to 128) from real users not knowing they'd be studied; open data and code.
- Strength: shows the time course: early steep drop, plateau, and what happens around breaks.
- Limitation: **no baseline and no control**: data starts at installation and covers only target apps, so it can't show whether total phone use fell or use moved to other apps (cf. kim2019lockntype's displacement).
- Limitation: survivorship: only people still using one sec could donate data; dropouts are invisible.
- Limitation: a co-author (Riedel) runs the company that makes one sec.
- Limitation: self-selected users who already want to cut down; demographics only for the 24% who answered the survey; no time zones, so no time-of-day analysis.

## How it relates to my thesis

The strongest long-term evidence for light friction before opening an app: a few seconds plus an explicit "close it" option made openings rarer and more intentional, and people kept using it for months, unlike lock-outs (tran2019, kim2019goalkeeper). It complements kim2019lockntype (task-based friction, launches halved) and fits lyngs2019's delay gap. Two cautions for any intervention: the effect seemed to stop as soon as the friction was turned off, so it supports behaviour rather than building a lasting habit (contrast mongeroffarello2021's residual effect), and users habituate to a fixed wait, the same issue as kasturiratna2025's memorised passcode. Methodologically, the plateau after ~3 weeks gives a reference for how long an evaluation should run, while the lack of baseline and non-target logging is exactly what a prototype with full Android usage logging could address. Also supports feature-level targeting (cho2021), since users wanted to separate Instagram's messages from its feed.

## Quotes / figures worth citing (with section)

- "the short design frictions introduced by one sec effectively reduce how often users attempt to open target apps and lead to more intentional app-openings over time." (Abstract)
- "These results suggest that the impact of the design friction does not last beyond its application." (Discussion, 5.4)
- "After using the app for a couple months I think my brain has gotten used to the waiting before an app opens." (P162, Results 4.3)
- "the decrease in app open attempts begins to flatten after approximately 20 days of use (roughly 3 weeks)." (Discussion, 5.3)
- Fig. 1: one sec flow. Fig. 6: open attempts and dismissal rate over time. Fig. 9–10: usage around breaks.
