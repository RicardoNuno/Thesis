# Search strategy

## Research areas and keywords

- **Dependency and overuse:** "smartphone dependency", "problematic smartphone use", "smartphone addiction", "smartphone overuse", "nomophobia"
- **Usage patterns:** "smartphone pick-ups", "phone checking habits", "screen time", "smartphone usage logging"
- **Interruptions and attention:** "mobile notifications", "notification interruptions", "self-interruption", "attention fragmentation"
- **Effects:** "smartphone use wellbeing", "productivity", "sleep", "focus"
- **Existing interventions:** "digital wellbeing", "screen time interventions", "app limits", "digital detox"
- **Phone replacement and alternatives:** "smartphone alternatives", "dumbphone", "minimalist phone", "feature phone", "smartphone non-use", "smartphone abandonment", "device substitution", "post-smartphone", "beyond the smartphone"
- **Minimalist phones:** Light Phone, Punkt MP02, Mudita Kompakt, Balance Phone, Wisephone
- **Open and unrestricted phones:** PinePhone, Librem 5, Volla Phone, Fairphone with /e/OS, "Linux phone", "user control over mobile OS", "app blocking Android", "device owner mode"
- **Smartwatches and the phone:** "smartwatch smartphone use", "phone checking", "standalone smartwatch", "LTE smartwatch", "cellular smartwatch", "smartwatch digital wellbeing", "smartwatch notifications", "smartwatch usage in the wild", "multi-device ecology"
- **History and evolution:** "history of the mobile phone", "evolution of mobile computing", "PDA to smartphone", "smartphone adoption", "diffusion of smartphones", "domestication of mobile technology", "ubiquitous computing", "always-on connectivity", "mobile phone as extension of the self"
  - Starting point: Mark Weiser, "The Computer for the 21st Century" (1991)

Combine with AND/OR, e.g. `("smartphone" OR "mobile phone") AND ("dependency" OR "problematic use" OR "overuse")`.

## Databases

- PubMed: psychology and health side (dependency scales, wellbeing effects)
- Google Scholar: broad coverage, grey literature and citation chasing
- ACM Digital Library: HCI-oriented studies (CHI, MobileHCI, UbiComp)

For minimalist and open phones, most material will be product pages, reviews and press rather than papers.

## Inclusion criteria

- Published 2010 or later, except foundational and historical work
- Peer-reviewed papers, plus key reports for statistics
- English
- Measures or discusses smartphone use, dependency or its effects, or alternatives to the smartphone

## Exclusion criteria

- Purely clinical addiction studies with no link to everyday use
- Short abstracts, posters, or no full text available

## Technique

Start from a few seed papers, then follow references (backward) and citing papers (forward).

## Search log

| Date | Database | Query | Hits | Kept |
| ---- | -------- | ----- | ---- | ---- |
| 2026-09-29 | PubMed | `(smartphone[tiab] OR "mobile phone"[tiab]) AND ("problematic use"[tiab] OR "problematic smartphone use"[tiab] OR dependency[tiab] OR addiction[tiab] OR overuse[tiab]) AND (systematic review[pt] OR meta-analysis[pt]) AND 2010:2026[dp]` | 111 | 1 (top 10 screened) |
| 2026-09-29 | PubMed | `("problematic smartphone use"[tiab] OR "smartphone addiction"[tiab]) AND (sleep[tiab] OR attention[tiab] OR "well-being"[tiab] OR wellbeing[tiab] OR depression[tiab]) AND meta-analysis[pt]` | 16 | 3 (top 10 screened) |
| 2026-09-29 | PubMed | `nomophobia[tiab] AND (systematic review[pt] OR meta-analysis[pt])` | 9 | 2 |
| 2026-09-29 | PubMed | `("smartphone use"[tiab] OR "screen time"[tiab]) AND ("self-report"[tiab] OR "self-reported"[tiab]) AND (objective[tiab] OR logged[tiab] OR tracking[tiab]) AND 2010:2026[dp]` | 428 | 0 (top 10 screened; off-topic, better in ACM DL) |
| 2026-09-29 | PubMed | `(smartphone[tiab]) AND ("digital detox"[tiab] OR abstinence[tiab] OR "screen time reduction"[tiab] OR "reduce smartphone use"[tiab] OR "digital wellbeing"[tiab]) AND 2010:2026[dp]` | 280 | 2 (top 10 screened; mostly smoking cessation noise) |
| 2026-09-29 | Google Scholar | `"smartphone" "pick-ups" OR "checking behavior" logged usage` | - | 9: wilcockson2018, ohme2021, gerlach2020, tng2024, cho2021, jonesjang2020, nesi2026, kim2019lockntype, kasturiratna2025 |
| 2026-09-29 | Google Scholar | `"self-reported" vs "logged" smartphone use` | - | 4: parry2021, deng2019, hitcham2023, james2023 |
| 2026-09-29 | Google Scholar | `allintitle: smartphone habits OR habitual checking` | - | 0 |
| 2026-09-29 | Google Scholar | `"dumbphone" OR "minimalist phone" OR "feature phone" wellbeing` | - | 4: schraggeova2025, parry2025, rosenberg2022, chia2021 |
| 2026-09-29 | Google Scholar | `"smartphone non-use" OR "smartphone abandonment" OR "giving up smartphone"` | - | 5: aranda2018, hiniker2016, ko2015, tran2019, haliburton2024 |
| 2026-09-29 | Google Scholar | `app blocking Android "accessibility service" OR overlay "digital wellbeing"` | - | 5: datta2022, lu2024, parry2023, almourad2021, mongeroffarello2021 |
| 2026-09-29 | Google Scholar | `"user control" mobile operating system restrictions` | - | 0 (too generic: privacy, law, robotics) |
| 2026-09-29 | Google Scholar | `"history of the mobile phone" OR "evolution of the smartphone"` | - | 3: agar2013, dunnewijk2007, evans2019 |
| 2026-09-29 | Google Scholar | `"domestication" smartphone everyday life` | - | 2: haddon2011, dereuver2016 |
| 2026-09-29 | Google Scholar | `"ubiquitous computing" Weiser smartphone vision` | - | 1: rogers2006 |
| 2026-09-29 | Google Scholar | `"minimalist phone" OR "digital minimalism"` | - | 3: newport2019, aylsworth2021, skorupska2026 |
| 2026-09-29 | Google Scholar | `"mere presence" smartphone cognitive capacity` | - | 3: ward2017, parry2024brain, wilmer2017 |
| 2026-09-29 | Google Scholar | `smartphone "task switching" OR "self-interruption" productivity` | - | 1: kim2017pomodolock |
| 2026-09-29 | Google Scholar | `"attention fragmentation" mobile phone` | - | 1: anderson2018 |
| 2026-09-29 | Google Scholar | `smartphone distraction work performance` | - | 2: duke2017, mark2018 |
| 2026-09-29 | Google Scholar | `"self-interruption" smartphone` | - | 0 |
| 2026-09-29 | Google Scholar | `"internal interruptions" OR "self-initiated" phone use` | - | 1: leiva2012 |
| 2026-09-29 | Google Scholar | `"post-smartphone" OR "beyond the smartphone"` | - | 0 (mostly AR/6G futures) |
| 2026-09-29 | Google Scholar | `"after the smartphone" future personal computing` | - | 1: goggin2025 |
| 2026-09-29 | Google Scholar | `"Light Phone" OR "Mudita" OR "Punkt" phone` | - | 4: jansson2024, ghita2021, silchenko2025, agnihotri2023 |
| 2026-09-29 | Google Scholar | `"e-ink phone" OR "e-paper phone"` | - | 0 |
| 2026-09-29 | Google Scholar | `"designer dumbphone"` | - | 0 (only already-listed papers) |
| 2026-09-29 | Google Scholar | `"Linux phone" OR PinePhone OR "Librem 5"` | - | 2: berker2023, knoll2021 |
| 2026-09-29 | Google Scholar | `"de-googled" Android OR "/e/OS" OR LineageOS` | - | 0 |
| 2026-09-29 | Google Scholar | `Android "device owner" OR "device policy" restrictions` | - | 1: mayrhofer2021 |
| 2026-09-29 | Google Scholar | `"Google Play" restrictions sideloading developer` | - | 0 (legal/competition papers) |
| 2026-09-29 | Google Scholar | `"PDA" smartphone convergence history` | - | 1: woyke2014 |
| 2026-09-29 | Google Scholar | `"always-on" OR "perpetual contact" mobile phone` | - | 3: bittman2009, mascheroni2016, hall2012 |
| 2026-09-29 | Google Scholar | `smartphone "extended self" OR "iSelf"` | - | 3: clayton2015, belk2013, ross2021 |
| 2026-09-29 | Google Scholar | `"mobile phone" "extension of the self"` | - | 0 (only already-listed papers) |
| 2026-09-29 | Google Scholar | `"standalone smartwatch" OR "LTE smartwatch" OR "cellular smartwatch"` | - | 0 (only health apps and antenna design; no study of watch as phone replacement) |
| 2026-09-29 | Google Scholar | `smartwatch "phone checking" OR "smartphone use" reduce` | - | 7: mcmillan2017, visuri2021, chen2021, lee2020pass, olson2022nudge, schmuck2020, vanvelthoven2018 |

Google Scholar hit counts not recorded; Scholar only gives rough estimates.
