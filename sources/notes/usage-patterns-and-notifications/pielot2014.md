# pielot2014: An in-situ study of mobile phone notifications

**Authors / venue / year:** Pielot, Church & de Oliveira / MobileHCI '14, pp. 233–242 / 2014
**Link:** https://doi.org/10.1145/2628363.2628364
**Relevance:** medium

## Summary (3 sentences)

One-week field study logging every notification on 15 Android phones, plus a daily diary on how notifications felt. Participants got ~65 notifications a day (mostly messengers and email), viewed most within minutes, and silent mode did not slow this down. More email and social network notifications correlated with stress and feeling interrupted, while more messages correlated with feeling connected; social pressure to reply fast was the main reason given.

## Method

- N = 15 Android users (6 F, 9 M), age 24–43 (median 28), North America / Europe; 27 started, 12 dropped for missing diary entries. Feb–Mar 2013.
- "Notification Monitor" app via the accessibility API: logged notification arrival and when it was *viewed* (drawer opened or app opened). Replies not logged.
- Whitelist of true push notifications (removed 64 apps, e.g. keyboard, download progress); 33 apps in 4 categories: messengers, email, social, other.
- Daily morning diary (9 questions): perceived volume, emotions, stories. Spearman correlations between daily logs and diary.

## Results / evidence

- 6854 notifications in 105 person-days; 65.3/day in Results (abstract and conclusion say 63.5). Messengers 3340, email 2210, other 1035, social 269. 78.4% on weekdays.
- Email peaks in working hours; messages at lunch and after work.
- Median time to view: 3.5–6.6 min messengers, 3.8–7.0 min social, up to 27.7 min email at weekends. Screen was off for 69.2% of arrivals → notifications often start a phone interaction.
- 70.6% first viewed in the drawer; from the drawer, only 41.1% went on to open the app.
- Ringer mode: 46.2% normal, 41.5% vibrate, 12.2% silent. Vibrate fastest; silent **not** slower than normal.
- Participants felt their ~65/day was "the usual" amount.
- Email volume ↔ stressed (ρ = .36), interrupted (ρ = .50), annoyed (ρ = .41), pressure to respond (ρ = .40). Social updates similar but weaker. Messages ↔ feeling connected (ρ = .29).
- Reasons for fast replies: others' expectations (read receipts), time-critical coordination, closeness of the relationship.
- Actual view times were faster than participants thought they were.

## Strengths / limitations

- Strength: real notifications logged in situ, not artificial ones from experience sampling.
- Limitation: 15 people, 1 week, adults; one-off snapshot from 2013 (WhatsApp volume grew 5× that year).
- Limitation: "viewed" is a lower bound (glancing at the status bar or reading on a desktop is missed); responses not logged.
- Limitation: inconsistent daily mean (63.5 vs 65.3) between sections.

## How it relates to my thesis

Shows how notification data can be logged on Android (accessibility API then, NotificationListenerService now) and what to measure: arrival, time to view, ringer mode. Silent mode not slowing viewing agrees with heitmayer2021 and oulasvirta2012: people check anyway, so muting alone does not reduce use. The authors themselves predict that cutting notifications would just increase checking. Also a counterweight: messaging notifications have a positive side (connectedness), so blanket blocking is not the answer.

## Quotes / figures worth citing (with page)

- "When notifications arrived, the screen had been off in 69.2% of the cases. Given how fast people attended to notifications, this indicates that notifications often triggered interaction with the phone." (p. 237)
- "it appears that having the phone in silent mode does not appear to help escape the effects of notifications." (p. 238)
- "even if these notifications are reduced, it's likely that mobile users will check their phones more frequently to make sure that no 'important' or 'urgent' message has been missed." (p. 241)
- "Notifications were largely checked within a few minutes of arrival, regardless of whether the phone was in silent mode or not." (p. 241)
- Table 1 (p. 236): notifications by category and top apps. Fig. 4 (p. 237): median time to view by category.
