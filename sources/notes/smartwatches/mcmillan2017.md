# mcmillan2017: Situating Wearables: Smartwatch Use in Context

**Authors / venue / year:** McMillan, Brown, Lampinen, McGregor, Hoggan & Pizza / CHI '17, 3582–3594 / 2017
**Link:** https://doi.org/10.1145/3025453.3025993
**Relevance:** low

_Skimmed from the full text pasted from the ACM version._

## Summary (3 sentences)

Second paper from the same wearable-camera dataset as pizza2016 (12 first-time Apple Watch users, a month of use, last three days filmed: 168 hours, 1,009 watch uses), here analysing how context (time of day, presence of others, activity, location) shapes watch use. Use is shorter and more basic in company: in conversation people touch the watch less and mostly just check the time (65% of uses), and 76% of touch interactions happened when alone, while location (home vs work) made no significant difference. Of 146 watch uses during conversation, about a quarter involved a brief pause but only two led to a topic change, so the authors argue talk is robust to watch glances and propose context-aware notification timing (e.g., delaying non-urgent alerts while the wearer is talking).

## Method

- Same participants and data as pizza2016: 12 iPhone users (7 women, aged 23–36), new to smartwatches, ≥28 days with an Apple Watch; two wearable cameras (forward and wrist) for the final days; 35 recording days (24 workdays, 11 weekend days); interviews.
- Each use coded for length, instigator, social context (alone / with others / in conversation), activity (Bureau of Labor Statistics time-use categories, collapsed to seven), location, app, notification source; 940 uses analysed after removing 69 where the screen was not visible.
- Repeated-measures ANOVA and logistic regression; conversation pauses coded after Newman et al. (topic retained vs changed); 110 clips analysed qualitatively.

## Results / evidence

- 5.3 uses per hour (8am–11pm), peaks around 1pm, 6pm and 9pm; mean 6.9 s, median 2 s (vs a 38 s median for phones in earlier work).
- Social context: alone 71% of uses, with others 13%, talking 15%; touch interactions 35% alone vs 25–27% with others; mean length 6.68 s alone, 6.62 with others, 5.01 in conversation; clock checks 50% alone vs 65% in conversation; notifications read less in conversation.
- Activity: socialising gives the shortest uses; eating alone the longest (the three longest uses, up to 3 min 24 s, were people eating alone in public); work uses unaffected by others' presence.
- Location: no significant effect (home 44%, outdoors 29%, work 14% of uses).
- Conversation: 32 of 146 uses (22–23%) involved a pause, only 2 with topic change or restatement; pauses ~4 s.
- 14% of watch uses happened alongside another screen ("second screening", e.g., reading messages while a phone call connects).
- Interviews: glancing at a watch can be read as being in a hurry ("Are you in a hurry? Do you have to go?"), so participants learned to manage it.
- Design ideas: delay non-urgent notifications while the wearer is talking; deliver low-priority ones in quiet moments; learn from dismissed notifications to hide or delay them; softer haptics for low priority; keep users in control rather than over-automating.

## Strengths / limitations

- Strength: observed behaviour with rich context, not self-report; separates presence of others from active conversation.
- Limitation: same small, novice, Stockholm-based sample and three filmed days as pizza2016, so it is not independent evidence.
- Limitation: only moments when the watch was used are sampled, so time in each context and ignored notifications are unknown.
- Limitation: some reporting slips: the conversation pause share is given as 22% and 23%; "in conversation" is 15% of uses in one table and 21.8% in another; one interaction is called significant with p = 0.13.

## How it relates to my thesis

Adds to pizza2016 that watch use adapts to social context and rarely disrupts conversation, which supports the idea that moving notification triage to the wrist is less socially costly than pulling out the phone (cecchinato2015, cecchinato2017). Its design suggestions, context-aware timing and learning which notifications the user dismisses, point to a smarter version of notification filtering for a watch companion. Because it shares data with pizza2016, cite the two together and do not count them as separate studies.

## Quotes / figures worth citing (with page)

- "Watch interaction is significantly shorter when the user is in conversation, than when alone." (Abstract, p. 3582)
- "Simply put, watch users are sensitive to the presence of others." (p. 3586)
- "Yet, in only two of these clips is there a change in topic or restatement. This suggests a strong robustness in talk to watch usage." (p. 3588)
- "it would be relatively straightforward to detect talk and delay the notification for a minute or two." (p. 3591)
- "key design interventions around context should consider using context while trying to keep users involved in decision making, rather than 'automating' excessively." (p. 3591)
- Fig. 2: social context vs touch and length (p. 3585); Fig. 3: app use by social context (p. 3586); Figs. 4–5: length by activity and location (p. 3587).
