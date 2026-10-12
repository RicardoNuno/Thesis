# andrews2015: Beyond Self-Report: Tools to Compare Estimated and Real-World Smartphone Use

**Authors / venue / year:** Andrews, Ellis, Shaw & Piwek / PLoS ONE 10(10), e0139004 / 2015
**Link:** https://doi.org/10.1371/journal.pone.0139004 (open access, CC BY)
**Relevance:** high

## Summary (3 sentences)

23 Android users had a simple screen on/off logger for two weeks, then estimated their daily use and number of pick-ups and filled in the Mobile Phone Problem Use Scale (MPPUS). They used the phone ~85 times and ~5 h a day; estimated duration correlated moderately with actual duration (r = .47), but estimated number of uses (37) was less than half the real number and did not correlate with it at all (r = .11). The MPPUS correlated with nothing, actual or estimated, so heavy use and problem use are not the same thing.

## Method

- 29 recruited (University of Lincoln staff and students, 17 F, mean age 22.5, range 18–33); 2 excluded for technical problems, 4 for missing estimates → 23 analysed.
- App built with Funf in a Box, "screen on/off" probe: timestamp when the phone becomes active and when it stops. Turned out to record *interactive state*, so calls and music with screen off count as use.
- Lab test: time to unlock and read an SMS. Nightly duration diary for 14 days (not analysed); at the end, estimates of average daily duration and number of uses, then MPPUS (27 items).
- Median use length per day to handle very long "on" periods (phone switched off is not logged). Matlab code for "barcode" plots and descriptives in S1 Appendix.

## Results / evidence

- 84.68 uses/day (SD 55.23), 5.05 h/day (SD 2.73); 55% of uses < 30 s.
- "Checks" defined as ≤ 15 s; peaks at 1–3 s, 5–6 s and 10–11 s. Unlocking and reading an SMS in the lab took 8.42 s.
- More uses in the afternoon and evening than morning and night; total duration and use length did not differ by time of day.
- Estimated vs actual uses: 37.20 vs 84.68 (t = 3.93, p < .001), r = .11 (n.s.).
- Estimated vs actual duration: 4.12 h vs 5.05 h (n.s.), r = .47 (p = .02).
- MPPUS: no significant correlation with any use measure (all p > .15), though 10 participants scored > 2 SD above the scale's norm.
- Checking rates similar to oulasvirta2012's 2009 data despite six years of smartphone growth.
- All but one used the phone as an alarm; last use before sleep → possible proxy for sleep length.

## Strengths / limitations

- Strength: real logged data, simple and cheap method, code shared.
- Strength: separates two kinds of estimate (duration vs frequency) and shows only frequency fails.
- Limitation: very small (n = 23), students and staff from one university, two weeks.
- Limitation: the probe counts calls and music as "use", and phone-off periods as long uses, so duration is inflated; this may also make the duration correlation look better than it is.
- Limitation: the nightly duration diary may have trained participants' final estimate (the authors admit this); no diary for number of uses.
- Limitation: inconsistent degrees of freedom (t(23), t(22), r(21)) for a sample of 23.
- Limitation: claims to be "the first paper to demonstrate that rapid mobile phone interactions are habitual", but it only shows people underestimate them; nothing tests habit (cues, automaticity).

## How it relates to my thesis

Strong support for logging rather than asking: people can roughly guess how long they use the phone but not how often they pick it up, and pick-up frequency is exactly the checking-habit measure (oulasvirta2012, heitmayer2021). Gives an empirical cut-off for a "check" (≤ 15 s, below oulasvirta2012's 30 s) and shows screen on/off events alone already reveal a lot. The MPPUS result backs the panova2018 / kwon2013sas critique: problem-use scales do not track actual use. Also a warning for my logging design: record screen state, not "interactive state", and handle shutdowns explicitly. Follow-up from the same group: ellis2019.

## Quotes / figures worth citing (with page)

- "Any subjective estimate is also likely to ignore rapid, yet pervasive, checking behaviours" (p. 2)
- "there were far more actual phone uses (84.68) than were estimated (37.20 [...]), and no significant correlation between the two" (p. 6)
- "for exploring checking behaviours, estimated number of uses show little reliability for measuring actual uses." (p. 6)
- "our data suggest that habitual goal-and reward-based actions are likely to be less than 15 seconds in duration" (p. 6)
- "heavy users are not necessarily the same as problem users. [...] research into smartphone use should identify heavy use and problem use independently of one another" (p. 7)
- Fig 1 (p. 3): two-week "barcode" of phone use. Fig 3 (p. 5): checks in 0.5 s bins with three peaks. Table 1 (p. 7): correlations of MPPUS, actual and estimated use.
