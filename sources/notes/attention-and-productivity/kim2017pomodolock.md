# kim2017pomodolock: Technology Supported Behavior Restriction for Mitigating Self-Interruptions in Multi-device Environments

**Authors / venue / year:** Kim, Cho & Lee / Proceedings of the ACM on Interactive, Mobile, Wearable and Ubiquitous Technologies (IMWUT) 1(3), Article 64, 21 pp. / 2017
**Link:** https://doi.org/10.1145/3130932
**Relevance:** medium

## Summary (3 sentences)

After interviewing 16 graduate students, who found self-interruptions (social media, shopping, YouTube) far harder to resist than notifications, the authors built PomodoLock: a 25-minute Pomodoro timer synced across PC, browser and Android phone that blocks the apps and sites the user puts on their own blocklist. In a 3-week field study (n = 36), the group whose blocklist actually blocked felt *less* coerced and less stressed than the timer-only group, because blocking removed the effort of resisting temptation themselves. The key condition was user control: users chose what to block, could edit the list any time and could stop the timer, and almost all said a non-stoppable version would be too coercive.

## Method

- Formative interviews: 16 graduate students who felt unproductive.
- PomodoLock: synced 25-min timer (Windows app, Chrome extension, Android service via Firebase); during a session, apps/sites on the user's blocklist are closed or redirected and the phone goes silent; user can stop the timer at any time, which unblocks everything.
- Field study: 40 graduate students (36 analysed; 31 M), Windows + Chrome + Android users, ~$30. Week 1 timer only for everyone; matched on week-1 sessions into control (timer + blocklist that did not block, framed as self-reflection) and experimental (timer + working blocker) for weeks 2–3.
- Measures: completed Pomodoro sessions, browser logs during sessions, perceived coercion and stress (exit survey), 20–25 min interviews.

## Results / evidence

- Blocklists: experimental group listed more (smartphone 8.1 apps vs 1.0; web 2.7 vs 0.9); a few blocked every phone app. Instant messengers were mostly left off: needed for work and social contact, and seen as deferrable.
- Sessions/day: 2.96 vs 2.09 (+41.5%, d = 0.54, n.s. over two weeks; significant in week 1 only). For low achievers the blocker helped (d = 0.78, p = .033); for high achievers no difference.
- More than half in both groups tried to open blocklisted sites during sessions, mostly out of habit; the control group spent ~111 s per session on them.
- Perceived coercion: control 3.22 vs experimental 2.44 (p = .038); stress 2.83 vs 2.28 (p = .037), on 1–5.
- Coercion split into external (from the tool) and internal ("self-coercion", effortful resistance). With the blocker, internal coercion fell from 5.1 to 3.3 (d = 1.52) and stress from self-resistance from 3.6 to 1.9 (d = 1.62); stress from the tool's restrictions rose (2.4 → 3.2) but stayed below neutral.
- "It is fully under my discretion; why should I feel coerced?" 16/18 in the experimental group said a version without a stop button would be too coercive and they would then leave communication apps and useful sites off the list.
- Multi-device blocking mattered: block Facebook on the PC and people use it on the phone.
- People often forgot to start sessions → the tool relies only on internal triggers; authors suggest external nudges.

## Strengths / limitations

- Strength: real multi-device tool in the field with a control group; separates internal vs external coercion, which explains why blocking can feel less coercive.
- Strength: clear design lesson on user control over what and when to block.
- Limitation: small, homogeneous sample (36 Korean graduate students, mostly male, Windows/Chrome/Android only); 2-week intervention.
- Limitation: main outcome (sessions completed) n.s. overall; coercion and stress are single self-report items.
- Limitation: control group's non-blocking blocklist may have frustrated them, inflating their coercion scores.
- Limitation: some reporting inconsistencies (Table 4 text says blocker coercion "slightly higher" with numbers in the opposite order; participants who blocked all apps named as E1/E8 in one place and E2/E14 in another; "sixteen" vs 18 in the experimental group).

## How it relates to my thesis

Most important point for my design: **give the user control over what is restricted**. Self-chosen blocklists, editable at any time, time-limited and stoppable, made restriction feel supportive instead of coercive, which complements tran2019 (people want lock-outs but don't adopt them) and cho2021 (blocking frustrates because it ignores context). The internal vs external coercion split is a useful argument: a tool that takes over the effort of resisting can lower stress, as long as the user stays in charge (fits the dual-systems view in lyngs2019). Also shows self-interruptions are the hard problem, not notifications, and that blocking only one device leaks to the other, which is relevant if a smartwatch is part of my setup.

## Quotes / figures worth citing (with page)

- "The findings suggest that when the coerciveness of behavioral restriction is appropriately controlled, coercive design can positively assist users in achieving their goals." (Abstract, p. 64:1)
- "I can unblock any application or website any time. It is fully under my discretion; why should I feel coerced?" (E11, p. 64:16)
- "The control over both time and the sources gave them a sense of freedom" (p. 64:17)
- "technology can either "share" one's burden of self-control or "empower" one's total energy source for self-regulation." (p. 64:17)
- "as long as external coercion mechanisms contribute to achieving the overarching goal (e.g., blocking to mitigate self-interruptions), users are likely positively to accept such behavioral constraints as assistive tools for maintaining intended behaviors." (p. 64:17)
- Table 3 (p. 64:15): coercion and stress by group. Table 4 (p. 64:16): internal vs external coercion.
