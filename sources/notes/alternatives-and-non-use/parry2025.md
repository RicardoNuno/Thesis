# parry2025: Connect to disconnect: What an online community for digital disconnection can tell us about digital well-being

**Authors / venue / year:** Parry, Kuit, Murray & van der Westhuizen / New Media & Society 28(8), 4303–4323 / 2025 (issue 2026)
**Link:** https://doi.org/10.1177/14614448251362436 (open access; preprint: https://osf.io/xyagz)
**Relevance:** medium

_Skimmed from the PsyArXiv preprint (v2), so wording and numbers may differ slightly from the published version; quotes cite sections._

## Summary (3 sentences)

Mixed-methods analysis of all r/NoSurf posts and comments from 2019–2021 (~94,000 after cleaning, by ~26,000 active members), using a structural topic model with 10 topics followed by qualitative reading of the top 1,000 documents per topic. Members wanted to disconnect because of online toxicity, platforms' role in societal problems, use of the internet as an escape from anxiety and depression, shallow online friendships and eroded attention; their practices were offline hobbies, blocking apps and websites, and dumbphones, and their challenges were deciding whether to delete accounts and quitting things they described as addictions. Almost nobody sought total withdrawal; the authors frame disconnection as a skilled self-regulation "literacy", mapped to the process model of self-control (situation selection, situation modification, cognitive change), while noting it rests on a medicalised, individual-responsibility discourse.

## Method

- Data: Pushshift API, all r/NoSurf content 1 Jan 2019 – 31 Dec 2021 (most active period, includes COVID-19): 112,398 items (7,993 posts, 104,405 comments); removed deleted users, bots and items under 10 words → 94,358.
- Lemmatised nouns, verbs and adjectives; trimmed very common (>40%) and rare (<1%) terms → 2,188-term dictionary.
- Structural topic model (stm in R) with post/comment and date as covariates; K chosen from 5–50 by held-out likelihood, residuals, exclusivity and coherence → K = 10; each document assigned to its highest-probability topic.
- Qualitative reading of the 1,000 most representative documents per topic (with thread context) to label and describe each topic; no formal coding. Scripts on OSF; data not shareable under Reddit's terms.

## Results / evidence

- Topic prevalence: alternative hobbies and routines 15.6% (31% of active members contributed), online toxicity 15.5%, technology and societal issues 12.2%, tech as escape from anxiety/depression 11.6%, dumbphones 11.4%, blocking apps/websites 9.6%, illusion of online friendship 7.7%, quitting struggles (social media, internet, pornography) 7.3%, attention-grabbing internet 4.9%, deleting/deactivating accounts 4.1%.
- Escape cycle: using the internet to cope, feeling guilty, then going back online to escape the guilt; internet often seen as a coping tool that became a trap rather than the root cause.
- Blocking: aimed mainly at staying focused at work; members agreed willpower alone fails and shared browser plugins, apps, system features and custom scripts (e.g. removing YouTube recommendations).
- Dumbphones: used as a pre-emptive strategy, but most kept a smartphone stored away for banking and similar tasks; others replaced single functions (e.g. an alarm clock so the phone stays out of the bedroom).
- Account decisions: people wanted to keep messaging but lose feeds; Reddit itself seen as an "attention trap" but less toxic than "comparison platforms" (TikTok, Instagram, Twitter, Facebook).
- Addiction framed literally ("rewired brains", dopamine, "cold turkey"), with blame on platform design and dark patterns, but members also urged dealing with underlying problems.
- Most contributors were passive: ~26,000 active out of ~200,000 members.

## Strengths / limitations

- Strength: very large, naturally occurring corpus; combines topic modelling with close reading; ties practices to a self-control theory; scripts shared.
- Strength: shows which disconnection strategies people actually discuss and how they combine them.
- Limitation: unknown demographics (Reddit skews young, male, US); only active posters, a vocal minority of members.
- Limitation: text only, no measures of whether strategies worked; topic shares measure talk, not behaviour.
- Limitation: data end in 2021 (pre-dates Pushshift closure) and cover the COVID-19 period; minor inconsistency in member counts (~200,000 vs 229,000 in 2024).

## How it relates to my thesis

Gives a large-scale view of what people who want to cut down actually do, which can inform what an intervention should offer: most want selective, not total, disconnection (keep messaging, lose feeds; block specific apps during work), which supports feature-level rather than app-level control (cf. cho2021, datta2022, lu2024's future work). Members' consensus that willpower is insufficient matches the case for friction and pre-commitment tools (haliburton2024, kim2019lockntype), and the dumbphone-plus-stored-smartphone pattern echoes rothschild2024's offloading. The process model of self-control (situation selection, modification, cognitive change) is a useful framework for classifying intervention types in the state-of-the-art chapter. The authors' critique that this discourse makes well-being an individual responsibility is worth noting when positioning a self-help app.

## Quotes / figures worth citing (with section)

- "This research characterizes digital disconnection not as mere avoidance, but as a dynamic, skillful, and individually negotiated practice, or literacy" (Abstract)
- "In almost all cases, it was evident that members were cognisant that willpower alone was insufficient to regulate their behaviour" (Findings, Methods to block apps/websites)
- "Those that used dumbphones for their day-to-day communication tended to keep a smartphone stored away to use when they needed to access particular apps/services that required a smartphone." (Findings, dumbphones)
- "Messaging features were generally regarded to contribute positively to peoples' lives ... while other features were deemed to be largely devoid of utility." (Findings, deleting/deactivating accounts)
- "the 'paradox' of using digital tools to disconnect is less a theoretical novelty and more a lived, practical necessity." (Discussion)
- Table 1: the 10 topics with prevalence and share of contributors.
