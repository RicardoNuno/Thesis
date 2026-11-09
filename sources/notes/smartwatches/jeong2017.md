# jeong2017: Smartwatch Wearing Behavior Analysis: A Longitudinal Study

**Authors / venue / year:** Jeong, Kim, Kim, Lee & Jeong (KAIST) / PACM IMWUT 1(3), Article 60, 31 pages / 2017
**Link:** https://doi.org/10.1145/3131892 (author copy: https://ic.kaist.ac.kr/files/papers/jeong2017smartwatch.pdf)
**Relevance:** low

## Summary (3 sentences)

Fifty KAIST students received Apple Watches (theirs to keep) and their heart-rate and step data were collected for 203 days (Mar–Oct 2016); since the watch reports no worn/not-worn state, the authors trained a classifier on that data (91% accuracy at 8-minute granularity, 97% in a validation week) and combined it with a survey and interviews. Participants wore the watch on 172 of 203 days on average, about 10.2 hours a day with 3.2 take-offs a day, and fell into work-hour (58%), active-hour (30%) and all-day (12%) wearers; four stopped wearing it within the period. Reasons for not wearing were charging (forgetting it on the charger), sleep, aesthetics, social disturbance and burden of immediate responses, breakage worries and tracking inaccuracy; self-reports overestimated wear time (13.4 h) and underestimated take-offs (2.1/day).

## Method

- 50 college students, one model (Apple Watch), no payment beyond keeping the watch; data via HealthKit (heart rate, steps) for 203 days.
- Wear-state classifier from heart-rate and step features (ground truth collected; 91% accuracy; 97% on a week-long natural validation with four users).
- Metrics: daily wearing hours, take-off events, streaks, breaks, usage density; clustering of diurnal patterns.
- Survey (n = 47) and interviews on reasons for wearing and taking off.

## Results / evidence

- Worn 171.9 of 203 days on average; mean 10.18 h/day (SD 3.51); 3.17 take-offs/day; mean take-off ~55 min.
- Groups: work-hour wearers 58%, active-hour 30%, all-day 12%; breaks mostly short (often forgotten on the charger), on weekdays as well as weekends.
- Four participants abandoned the watch (wore it 12–85 days).
- Self-report vs data: wear time overestimated (13.38 h), take-offs underestimated (2.06/day).
- Reasons against wearing: charging routine, sleep comfort, aesthetics and formal settings, social disruption and pressure to respond, fear of breaking it, inaccurate activity tracking, gaming or typing comfort.
- Design implications: reminders to put the watch back on (e.g., Bluetooth/place detection), managing interruptions, using the watch for behaviour change; the authors suggest "we can nudge users of overuse by vibrating watches until the users stop using their phones".

## Strengths / limitations

- Strength: long (203 days), objective measure of wearing, with qualitative explanation; shows self-report error.
- Limitation: one watch model, college students in Korea, given free watches (novelty and selection effects).
- Limitation: wear state inferred, not measured; does not look at phone use at all.

## How it relates to my thesis

Only relevant if a watch companion is part of the design: it shows a watch is worn around 10 hours a day, not all day, with frequent short breaks (charging, sleep, home), so any watch-based intervention would be absent for much of the time, notably at night when phone overuse often peaks (shahu2024). It also proposes, without testing, the same vibrate-on-overuse idea that okeke2018 and shahu2024 tested and found irritating. Its self-report gap echoes parry2021 for phones.

## Quotes / figures worth citing (with section)

- "Our analysis results (n=50) showed that the mean daily wearing time were 10.18 hours (SD=3.51), and the mean number of take-off events per day was 3.17 (SD=1.11)." (§5.1)
- "Participants overestimated the mean wearing duration as 13.38 hours (SD=3.65), whereas they underestimated the mean number of take-off events per day as 2.06" (§5.1)
- "we can nudge users of overuse by vibrating watches until the users stop using their phones." (§5.2)
- Fig. 2: distribution of wearing days; wearer groups (work-hour, active-hour, all-day).
