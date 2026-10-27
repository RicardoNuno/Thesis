# anderson2018: A Survey of Attention Management Systems in Ubiquitous Computing Environments

**Authors / venue / year:** Anderson, Hübener, Seipp, Ohly, David & Pejović / Proceedings of the ACM on Interactive, Mobile, Wearable and Ubiquitous Technologies (IMWUT) 2(2), 27 pp. / 2018
**Link:** https://doi.org/10.1145/3214261 (preprint: https://arxiv.org/abs/1806.06771)
**Relevance:** medium

_Skimmed from the arXiv preprint; page numbers are preprint pages._

## Summary (3 sentences)

Survey of "attention management systems": systems that sense the user's context, model when they are interruptible, and then manage notifications (defer, change modality, choose device, or signal availability). It links cognitive theory (threaded cognition, ACT-R, memory for goals, problem state) to practice, concluding that interruptions hurt least at task boundaries or idle moments, and that users should be helped to rehearse and resume the interrupted task. It covers the sensors, features and machine-learning models used to infer interruptibility, and flags open issues: ethics and transparency, privacy, and the lack of long-term studies on well-being.

## Method

- Narrative survey (no systematic search protocol reported), structured as: definitions of attention and interruption → cognitive theories of multitasking → system pipeline (sensing → processing → inferring → modeling → managing) → implications and research questions (RQ1–RQ14).
- Scope: mainly **external** interruptions (notifications); internal interruptions (self-initiated checking) are mentioned but not the focus.

## Results / evidence

- Interruption structure: interruption lag → handling (immediate, negotiated, scheduled, mediated) → resumption lag. Four handling strategies.
- Theory → design: interrupt at breakpoints/low engagement (problem state free); allow rehearsal of the primary task before switching; give "psychologically close" cues to resume; match alert modality to the cognitive resource that is free (e.g. audio while visually busy).
- Sensing: Table 1 lists sensors and features used to infer interruptibility (accelerometer, microphone, app usage, screen events, time, location, physiological sensors like EDA/ECG/EEG); typical classifiers J48, SVM, k-means; cascading classifiers (activity → breakpoint → interruptibility).
- Models (Table 2): breakpoints (Okoshi/Attelia II), context (Pejović InterruptMe), engagement, attentiveness (Pielot), availability, mental workload; evaluated via ESM (often NASA-TLX) or implicit measures (time to react, e.g. "opportune" if handled within 10 min).
- Management (Table 3): mediating (defer to breakpoints), mitigating (choose device/modality), indicating (show availability).
- ~100 notifications/day per user; disabling them raises perceived productivity but also anxiety about responsiveness (Pielot & Rello).
- Ethics: systems must be transparent (inspect, override, disable) and interpretable (human-readable rules; >50% of rules accepted in Mehrotra et al.); privacy of rich sensor data.
- Well-being effects only shown in short studies (≤ ~2 months); long-term effects unknown.
- "even when notifications are disabled on their phones, people still self-interrupt, checking for new content in fear of missing out."

## Strengths / limitations

- Strength: good bridge from cognitive theory to concrete design rules; useful tables of sensors/features, models and strategies.
- Strength: explicit open research questions (ethics, transparency, long-term evaluation).
- Limitation: not systematic; covers literature to ~2017.
- Limitation: centred on external interruptions (notifications), while self-initiated checking is a candidate focus for my thesis.
- Limitation: physiological sensing and some systems discussed are lab-heavy and not deployable on commodity phones.

## How it relates to my thesis

Main reference for an AI / adaptive approach: it shows how phones already infer interruptibility from sensors and app usage with machine learning, and the pipeline (sense → infer → model → manage) is a good template for describing an adaptive intervention. Its design rules transfer to my case: intervene at breakpoints rather than mid-task, keep the logic transparent and overridable (matches kim2017pomodolock and mark2018 on user control), and evaluate beyond a few weeks. It also points to a gap: most attention management handles notifications, while self-interruptions persist even when notifications are off (heitmayer2021, kim2017pomodolock).

## Quotes / figures worth citing (with page)

- "systems that sense, model, and manage the attentional state of a user. Managing the attentional state is considered as any action of the system, which supports an individual to maintain its concentration on a task or activity." (p. 16)
- "interruptions need to arrive at task boundaries or during routine tasks, should allow for task state rehearsal, and support context retrieval through hints presented to the user after an interruption." (Key takeaways, p. 3)
- "even when notifications are disabled on their phones, people still self-interrupt, checking for new content in fear of missing out" (p. 17)
- "Individuals need to have the option to inspect, override, or to disable functional principles." (p. 17)
- Table 1 (p. 12): sensors and features. Table 2 (p. 14): interruptibility models. Table 3 (p. 16): management strategies. Fig. 4 (p. 10): system pipeline.
