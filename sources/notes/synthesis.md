# Synthesis: ideas and tier list

Cross-paper view of the reading (Sprint 1–2). Each idea lists the papers behind it and what it means for the thesis. Details, numbers and caveats are in the individual notes (`<folder>/<bibkey>.md`).

Thesis scope (from the proposal): survey the Android mechanisms for monitoring and intervening on smartphone use, then build at least one lightweight, consent-friendly intervention prototype and evaluate it on accuracy, battery, usability and acceptability against Google Digital Wellbeing.

---

## 1. Key ideas

### 1.1 The problem is checking, not only screen time
- Most phone use is short, self-initiated checking that becomes habitual and can spill into other apps (oulasvirta2012, heitmayer2021, ferreira2014, bohmer2011, nesi2026). Checks that find nothing still keep the habit going (skinner1948); compulsive sessions have identifiable start and end triggers (tran2019).
- Checking frequency and screen time are distinct measures with different correlates (wilcockson2018, tng2024).
- **Thesis:** measure pick-ups/opens as well as time; an intervention that only caps time misses checking (see 1.6).

### 1.2 Self-reports are unreliable; log behaviour
- Self-estimated use correlates weakly with logs (parry2021: r ≈ .38; problematic-use scales r ≈ .25), people misjudge use (andrews2015, ohme2021), scales barely track logged use (ellis2019, hitcham2023); the same happens for watch wear time (jeong2017).
- Logging needs careful session definitions and enough days (vanberkel2016, wilcockson2018).
- **Thesis:** "accuracy" in the evaluation means comparing the prototype's logged data with Digital Wellbeing and ground truth, not with users' estimates; outcomes should come from logs.

### 1.3 Harms are real but modest and debated; say "problematic use"
- Meta-analyses link problematic smartphone use (PSU) to depression, anxiety and poor sleep in a sizeable minority (sohn2019, yang2020, elhai2017, olson2022, chu2023, sunday2021); nomophobia is common (yildirim2015, almamun2025, leonmejia2021).
- Effects on well-being are small and "addiction" framing is contested (orben2019, panova2018, james2023, larsen2023); cognitive "brain drain" is weaker than first claimed (ward2017 vs parry2024brain; wilmer2017).
- Standard measures: SAS / SAS-SV (kwon2013sas, kwon2013sassv), NMP-Q (yildirim2015).
- **Thesis:** motivate with problematic use and lost control, avoid clinical "addiction" claims; SAS-SV is the obvious secondary outcome.

### 1.4 Notifications and the obligation to respond drive checking
- People receive many notifications and respond fast (pielot2014); a notification alone costs attention (stothart2015); disruption depends on content and timing (mehrotra2016, leiva2012, anderson2018).
- Users feel obliged to reply quickly (aranda2018's obligation cycle; cecchinato2017 on read receipts and reply expectations).
- **Thesis:** notification management is a lever on its own, not just app-time limits (see 1.8).

### 1.5 Use is valued selectively: people want to cut regretted parts, not everything
- Regret attaches to specific features and unintentional use (cho2021; aranda2018: "the less intentional the action, the more regret").
- Interventions that let users target what they see as wasteful reduce that use while valued use stays (hiniker2016).
- People want to keep messaging but lose feeds; they disconnect selectively, not totally (parry2025, baumer2013, rothschild2024).
- Feature-level control is technically possible but costly (datta2022 overlays; lu2024 future work).
- **Thesis:** user-chosen targets and, ideally, finer than whole-app control.

### 1.6 Friction before opening works and is accepted more than blocking
- Lockouts cut use but frustrate; weaker, overridable versions are preferred (kim2019goalkeeper); user-chosen, stoppable blocking feels less coercive (kim2017pomodolock); blocking suits some people and stresses others (mark2018).
- Friction at launch reduces opens: typing digits halves launches (kim2019lockntype), a 6 s pause leads to fewer, more intentional opens over 13 weeks (haliburton2024); slowing interaction after a limit cuts time and opens and is bypassed less than a lockout (lu2024).
- Acting only during use cuts time but not opens (okeke2018's vibration).
- Google's own researchers recommended overridable "speed bumps" and partial disconnection (aranda2018).
- **Thesis:** strongest evidence base for an intervention type: short, overridable friction at app launch.

### 1.7 Effects fade, habituate, and shift elsewhere
- Effects disappear when the intervention stops (haliburton2024, okeke2018, lu2024 break days) and drop after the first week (shahu2024, lee2026).
- Fixed nudges and repeated messages habituate or annoy (vanvelthoven2018, almourad2021, okeke2018, shahu2024); lu2024 ramps intensity to counter this.
- Time saved in one app moves to others or to longer sessions (kim2019lockntype, lu2024).
- Detox evidence is mixed and withdrawal/craving rise (radtke2021; wilcockson2019 as an example of weak design).
- **Thesis:** vary or ramp the intervention, measure whole-phone use, and include a withdrawal phase to test persistence.

### 1.8 Passive monitoring (Digital Wellbeing / Screen Time) is not enough
- Most people who "use" wellbeing tools only glance at reports; Android's Digital Wellbeing is used far less than iOS Screen Time; users and non-users report similar phone time (parry2023, schmuck2020).
- Reviews praise awareness and control but criticise inaccuracy, rigid limits and repetitive nudges (almourad2021); tracking alone barely changes use (olson2022nudge, mongeroffarello2019).
- **Thesis:** this is the gap against the Digital Wellbeing baseline: something that acts at the moment of use rather than reporting afterwards.

### 1.9 Settings and interface changes work without blocking
- Turning off notifications, greyscale, password unlock and hiding social apps cut use by about an hour a day vs tracking only, and stuck because they are "set and forget" (olson2022nudge); similar bundle, smaller effect on pickups (kasturiratna2025).
- A text-only launcher reduced habitual use and screen time (schraggeova2025).
- **Thesis:** low-permission options (launcher, guided settings changes) are realistic, consent-friendly baselines or components.

### 1.10 Motivation decides who benefits
- Minimal phones improved well-being only for volunteers, not for those assigned (lee2026); interventions work best for people who want to reduce use (hiniker2016, parry2023; schraggeova2025 participants; mark2018 by self-control).
- **Thesis:** measure motivation/readiness at baseline as a moderator; recruit with this in mind.

### 1.11 Android constraints shape what can be built
- Android's multi-party consent model routes cross-app monitoring through special-access permissions granted manually in Settings, plus Play Store restrictions (mayrhofer2021).
- Implementation patterns seen in the reading: UsageStatsManager for usage (shahu2024), foreground-app checks and vibration (okeke2018), Accessibility overlay with `dispatchGesture` (lu2024), screen capture over ADB + overlay (datta2022, research only), launcher replacement (schraggeova2025).
- Users may disable things that matter (Bluetooth off in shahu2024); battery is rarely reported (lu2024, shahu2024 silent).
- **Thesis:** the API comparison table (issue #15) should rank options by permission cost, Play Store risk, accuracy and battery; few permissions, requested when needed (mayrhofer2021 consent principles).

### 1.12 Dropping the phone is costly; non-use is a spectrum
- Dumbphone and minimal-phone users lose messaging and smartphone-only services (banking 2FA, ride-hailing) and offload them to people and devices (rothschild2024, parry2025, rosenberg2022); daily life is reorganised around the phone (aranda2018, haddon2011).
- Non-use ranges from limiting to leaving and relapsing (baumer2013); refusers object to the always-carried device, not content (rosenberg2022).
- Minimalism framed as intentional use, not abstinence (aylsworth2021); minimal devices are sold as "absence" (jansson2024).
- **Thesis:** supports reducing the phone's pull while keeping essential functions, rather than replacement.

### 1.13 Separation stress: the near-but-not-away dilemma
- The phone's presence lowers performance (ward2017, weaker in parry2024brain); separation from a ringing phone raises stress and lowers performance (clayton2015).
- **Thesis:** abrupt, forced separation can backfire (also lee2026's early dependency rise); prefer gradual, user-controlled measures and silencing over hiding.

### 1.14 The smartwatch as a lower-pull companion (open option)
- Watch interactions are very short (median 2–5 s) and only ~3% lead to phone use (pizza2016, visuri2017); owners triage notifications on the wrist instead of pulling out the phone (cecchinato2015, cecchinato2017, mcmillan2017); watch apps offer far fewer interactions (chen2021).
- Conditions: notifications must be filtered and routed, not mirrored (cecchinato2017, sahamishirazi2015, visuri2017, visuri2021); checking habits carry over as "peeks" (visuri2017); watches are worn ~10 h/day, not at night (jeong2017); battery suffers from frequent wake-ups (liu2017).
- Only one intervention study, a 6-person pilot: watch-face feedback helped, vibration alarms irritated (shahu2024); bolle2015 is anecdotal.
- No study logged phone use alongside watch use, so "less phone use" remains unproven.
- **Thesis:** a possible extension or future work, motivated by the "device not content" argument (rosenberg2022); would need paired phone–watch logging.

### 1.15 Framing and history
- Ubiquitous computing's "calm" vision (weiser1991) vs the call for technology that keeps people in control and prompts reflection (rogers2006); domestication and lock-in (haddon2011); post-smartphone device hype (goggin2025).
- **Thesis:** one or two paragraphs of context at most.

---

## 2. Tier list

Ranked by usefulness for the thesis and strength of evidence together. "Cite with care" items have notable flaws described in their notes.

**S: core, build arguments on these**
- Problem and measurement: oulasvirta2012, parry2021, heitmayer2021, tran2019, cho2021
- Interventions: haliburton2024, lu2024, kim2019lockntype, kim2019goalkeeper, hiniker2016, lyngs2019, olson2022nudge
- Platform and baseline: mayrhofer2021, aranda2018, parry2023

**A: strong support**
- Measurement and logging: andrews2015, ellis2019, hitcham2023, wilcockson2018, vanberkel2016, kwon2013sassv
- Effects and framing: sohn2019, elhai2017, olson2022, yang2020, orben2019, panova2018, james2023
- Attention: ward2017, kim2017pomodolock
- Interventions and tools: okeke2018, mongeroffarello2019, mongeroffarello2021, datta2022, almourad2021
- Alternatives: lee2026, rothschild2024, parry2025, schraggeova2025 (baseline imbalance)
- Smartwatch: cecchinato2017, pizza2016, shahu2024 (pilot, n = 6)
- Dependency: clayton2015 (confounded design)

**B: supporting or context**
- Usage and notifications: ferreira2014, pielot2014, stothart2015, mehrotra2016, ohme2021, tng2024, nesi2026, skinner1948, bohmer2011
- Attention and productivity: mark2018, anderson2018, parry2024brain, wilmer2017
- Effects: chu2023, larsen2023, sunday2021, almamun2025, leonmejia2021, yildirim2015, kwon2013sas
- Interventions: radtke2021, balhara2026, kasturiratna2025, ko2015, ko2016, schmuck2020 (cross-sectional)
- Alternatives: rosenberg2022, baumer2013
- Smartwatch: visuri2017, mcmillan2017 (same data as pizza2016)
- History: weiser1991, rogers2006

**C: cite-only, narrow or no data**
- duke2017, leiva2012 (dated), vanvelthoven2018 (not peer-reviewed, conflict of interest), aylsworth2021, jansson2024, goggin2025, haddon2011
- Smartwatch details: visuri2021, jeong2017, sahamishirazi2015, chen2021, cecchinato2015 (superseded by cecchinato2017)

**D: weak, avoid or use only as a negative example**
- wilcockson2019 (24 h, no control), bolle2015 (8 people, different comparison group), schirra2015 (5 interviews), liu2017 (energy/network, off-topic)
