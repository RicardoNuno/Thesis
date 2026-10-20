# parry2021: A systematic review and meta-analysis of discrepancies between logged and self-reported digital media use

**Authors / venue / year:** Parry, Davidson, Sewall, Fisher, Mieczkowski & Quintana / Nature Human Behaviour 5(11), 1535–1547 / 2021
**Link:** https://doi.org/10.1038/s41562-021-01117-5 (accepted manuscript: https://purehost.bath.ac.uk/ws/files/219658181/Final_Manuscript.pdf; data and code: https://osf.io/dhx48/)
**Relevance:** high

_Read from the accepted manuscript; page numbers below are manuscript pages, not journal pages._

## Summary (3 sentences)

Pre-registered meta-analysis of 47 studies (106 effect sizes) that measured digital media use both by self-report and by logs. Self-reported use correlates only moderately with logged use (r = .38), problematic-use scales correlate even less with logged use (r = .25), and only 3 of 49 comparisons had self-reports within 5% of the logged mean, with people over- and under-reporting about equally often. The authors conclude that self-reports are not a valid stand-in for logged use and that researchers should use logging whenever they make claims about usage.

## Method

- Pre-registered protocol (OSF); search returned 12,132 records → 47 included (45 published/preprints + 2 unpublished datasets).
- Three meta-analyses with robust variance estimation (RVE):
  - Self-reported vs logged use: 66 effects, 44 studies, N = 52,007.
  - Problematic-use scales vs logged use: 40 effects, 19 studies, N = 5,552.
  - Accuracy (ratio of self-reported to logged means): 49 comparisons, 30 studies, N = 17,523.
- Moderators: medium (phone vs social media), self-report form (scale vs single estimate), category (duration vs volume); post hoc: population, design, logging method.
- Quality: Q-SSP checklist, mean 66.6/100; 55.6% "acceptable". Egger tests and influence diagnostics for bias.

## Results / evidence

- Self-reported vs logged use: r = .38 [.33, .42]; very high heterogeneity (I² = 92%). No small-study bias; robust to removing outliers and non-peer-reviewed studies.
- No moderator explained the heterogeneity: phone vs social media, scale vs estimate, duration vs volume, population, design and logging method all n.s.
- Problematic-use scales vs logged use: r = .25 [.20, .29], low heterogeneity (I² = 29%) → consistently weak; these scales measure a different construct from use.
- Accuracy: only 3/49 (6%) within 5% of logs; 47% over-reported, 47% under-reported. Pooled ratio R = 1.21 [0.94, 1.54], n.s. → no consistent direction.
- Duration tended to be over-reported and volume (e.g. number of pickups) under-reported, but the difference was n.s. (p = .056).
- Other studies suggest the error is systematic: accuracy depends on how much people use and on their well-being (Sewall et al. 2020, cited by the authors).

## Strengths / limitations

- Strength: pre-registered, large evidence base, open data and code; robust to sensitivity checks.
- Strength: separates general use from problematic-use scales and tests direction of error, not just correlation.
- Limitation: most effects are phone or social-media studies; too few for internet, games or computer, so medium cannot really be tested.
- Limitation: heterogeneity left unexplained; moderator tests underpowered.
- Limitation: logs are treated as ground truth, but they have their own errors (background activity counted as use, coverage gaps, reactivity, privacy issues), as the authors admit.
- Limitation: many included studies are small convenience samples; non-normal usage data may slightly inflate correlations.

## How it relates to my thesis

The main citation for why my thesis must log usage instead of asking people: self-reports share only about 14% of variance with logs (r = .38), and almost nobody estimates their own use accurately. Pulls together the single studies already in my notes (andrews2015, ellis2019, ohme2021, hitcham2023) into one pooled result. The weak link between problematic-use scales and logs (r = .25) supports panova2018 and james2023: scales like the SAS-SV (kwon2013sassv) do not measure use itself, so I should not use them as a proxy for checking. It also supports showing people their logged usage as an intervention: if people cannot estimate their own use, feedback from logs gives them information they don't have. Their call to focus on specific behaviours rather than total screen time fits my focus on checks/pickups.

## Quotes / figures worth citing (with page)

- "we found that self-reported media use only moderately correlates with logged measurements, that self-reports were rarely an accurate reflection of logged media use, and that measures of problematic media use show an even smaller association with usage logs." (Abstract, p. 2)
- "Self-reports of behaviour are, consequently, an index of what respondents believe that they do—their perceptions of their own behaviour—and not necessarily what they actually do" (pp. 3–4)
- "less than 10% of self-reports are within 5% of the equivalent logged value, indicating that, when asked to estimate their usage, participants are rarely accurate." (p. 9)
- "it is time for researchers to stop pretending that self-reports are accurate indicators of actual behaviour" (p. 11)
- "researchers should endeavour to use a measure that most closely approximates the behaviour that they are targeting. In almost all cases, therefore, researchers should use tracking or logging services to measure media usage." (p. 11)
- Fig. 2: forest plot, self-report vs logs. Fig. 4: problematic use vs logs. Fig. 5: ratio of means.
