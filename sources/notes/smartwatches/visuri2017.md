# visuri2017: Quantifying Sources and Types of Smartwatch Usage Sessions

**Authors / venue / year:** Visuri, Sarsenbayeva, van Berkel, Goncalves, Rawassizadeh, Kostakos & Ferreira / CHI '17, 3569–3581 / 2017
**Link:** https://doi.org/10.1145/3025453.3025817 (author copy: https://zhannina.github.io/papers/chi17.pdf)
**Relevance:** medium

_Skimmed from the author-hosted version._

## Summary (3 sentences)

Large in-the-wild logging study of 307 Android Wear users (Jan–Jul 2016, via the Play Store app Insight 4 Wear): about 800,000 screen sessions and 2.8 million notifications, compared with an aggregated smartphone dataset of 445 users from four earlier studies. Watch use is brief and frequent: 65% of sessions are "peeks" of 5 s or less, 80% are user-initiated rather than triggered by a notification, and users with ≥7 days of data had about 142 sessions a day versus about 60 on phones, while phone sessions averaged nearly 4 minutes. Responses to notifications looked like those on phones (communication apps lead to longer interactions, maps/health to peeks), but notifications were acted on quickly (median delay 20 s), and only 9.4% of notifications led to a watch session.

## Method

- Data: anonymous Play Store users of Insight 4 Wear; screen on/off events (800,119) and notifications with source app (2,801,082); mostly North America and Europe; Moto 360, Huawei Watch, Sony SmartWatch 3, LG and others. Most users logged < 30 days (median 4 days); 18 logged > 90 days.
- Sessions = screen on → off, filtered at 5 min (0.2% removed as likely charging). Session "peek" ≤ 5 s (5 s is the watch's automatic screen timeout) vs "interaction" > 5 s; "notification-initiated" if within 60 s of a notification, else "user-initiated".
- App categories from the Play Store, grouped (Communication, Productivity & Admin, Health, Internet & Social, Maps and Travel, Media, Games, Other).
- Comparison: 347,576 smartphone screen events → 120,277 sessions from four earlier Oulu studies (2014–2016), with no notification or app data.
- Chi-square, ANOVA, t-tests; continuous sessions defined with a 45 s gap.

## Results / evidence

- 798,423 sessions: 65% peeks, 35% interactions; 80% user-initiated, 20% notification-initiated.
- Session length: notification-initiated mean 10.7 s, user-initiated 7.9 s; median 5 s; smartphone mean ~3 min 49 s (3 min 52 s in another place).
- ~142 watch sessions/day (users with ≥ 7 days) vs ~60 phone sessions/day in the comparison data.
- 81% of watch sessions were isolated (no follow-up within 45 s); repeated sessions got progressively shorter.
- Notifications: mostly Tools (38.5%), Travel and Local (21.9%), Communication (9%); only 9.4% led to a session; median delay 20 s (faster than ~30 s reported for phones); faster during daytime.
- Communication and Internet & Social notifications lead to interactions; Maps/Travel and Health to peeks; communication notifications preferred during the day, social in the evening.
- Authors suggest pushing to the watch only notifications whose required action can be done on the watch.

## Strengths / limitations

- Strength: by far the largest logged dataset on watch use; separates user- vs notification-initiated sessions.
- Limitation: sessions are inferred from screen-on, which also triggers on wrist raises, notifications and light; the 5 s "peek" equals the automatic timeout, so many peeks may not be deliberate use.
- Limitation: no data on the same users' phones, so it cannot show whether watches reduce phone use; the phone comparison is a different population and period.
- Limitation: self-selected tech enthusiasts who installed a logging app, most for only a few days; no demographics beyond region.
- Limitation: "an order of magnitude bigger" overstates 142 vs 60 sessions/day (about 2.4×).

## How it relates to my thesis

Quantitative backing for how a watch is used: lots of very short glances, mostly unprompted, while longer, content-creating use stays on the phone, consistent with pizza2016's camera data. For a watch companion, its key point is that checking habits carry over to the watch (frequent unprompted peeks), so a watch could replace phone checks with shorter ones rather than remove checking. It also supports filtering which notifications reach the watch (cecchinato2017). The missing link, whether phone use actually drops, still needs paired phone–watch logging, which is what an evaluation would have to do (cf. shahu2024).

## Quotes / figures worth citing (with page)

- "The results show that smartwatches are used more briefly and more frequently throughout the day, with half the sessions lasting less than 5 seconds." (Abstract)
- "We introduce a new term to describe these short usage sessions, peeks, in which the smartwatch is used for only five seconds or less." (Conclusion)
- "These results suggest that the habit of quick unprompted peeks (and micro-usage) seems to carry from smartphones to smartwatches" (Analysis and Results)
- "notifications that require interaction can be pushed to the smartwatch only if they are likely to be relevant for interaction methods available on the smartwatch." (Discussion)
- Fig. 3: session categories; Fig. 10: session length smartwatch vs smartphone; Fig. 16: daily session counts, watch vs phone.
