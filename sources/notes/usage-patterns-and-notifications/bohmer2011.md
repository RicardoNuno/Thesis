# bohmer2011: Falling asleep with Angry Birds, Facebook and Kindle: a large scale study on mobile application usage

**Authors / venue / year:** Böhmer, Hecht, Schöning, Krüger & Bauer / MobileHCI '11, pp. 47–56 / 2011
**Link:** https://doi.org/10.1145/2037373.2037383 (author copy: https://brenthecht.com/publications/bhecht_mobilehci2011_sleepbirds.pdf)
**Relevance:** low–medium (historical baseline; data from 2010)

## Summary (3 sentences)

A background "AppSensor" inside an app-recommender app (appazaar) polled the foreground app twice a second while the screen was on, for 4,125 Android users over 163 days (Aug 2010 – Jan 2011, 22,626 apps, 4.92 M samples). Users spent ~59 min/day on apps but only ~72 s per app session; 68% of "app chains" (sessions until > 30 s of standby) used a single app, and half lasted under 5 s. Communication apps dominated the day and opened half of all sessions, news peaked in the morning, games and social apps late at night, and app sessions were longest at night.

## Method

- AppSensor: polls the most recently started app every 500 ms while the screen is on; standby time removed. Background apps (music) and widgets not captured.
- Distributed via Android Market as part of appazaar (no payment, no demographics, hashed IDs); advertised on Facebook, Twitter, Gizmodo, ReadWriteWeb.
- Apps categorised with Android Market categories (games merged; browser, settings separate; launchers removed).
- App chain = apps used without > 30 s of standby in between (1.84 M chains). Descriptive stats by hour, category, location (airports, speed > 25 km/h, US vs Europe).

## Results / evidence

- 59.23 min/day; mean app session 71.56 s (Finance 31.9 s, Libraries & Demos 274 s).
- Chains: 68.2% one app, 19.5% two, 6.6% three; 49.8% shorter than 5 s.
- First app of a chain: Communication 49.6% (SMS 15.7%, phone 9.6%, email 5.9%); browser only 5.9%.
- After any app, next app is Communication with p ≥ .23 (except News, Lifestyle); Communication → Communication 66.5%.
- Launches peak ~18:00, minimum ~05:00 (still 16% of peak); session length is the inverse, longest ~05:00 (6.3 min), shortest ~17:00 (~40 s).
- News peaks 7–9 h; games and social 21–01 h; Kindle late evening; weather and calendar morning; alarm clock apps "used" 2–9 h (screen kept on).
- Airports: browser 2.78× more likely; moving > 25 km/h: multimedia 2.26×.

## Strengths / limitations

- Strength: very large, in-the-wild, real logged foreground app data; first of its kind; defines a usable session ("chain") with a 30 s gap.
- Limitation: **old**. Data from 2010 (Android 2.x, pre-WhatsApp/Instagram dominance); ~1 h/day vs ~4–5 h/day in andrews2015 and ellis2019, so the absolute numbers do not describe current use.
- Limitation: sample = early adopters who install an app-recommender; no demographics.
- Limitation: polling the "most recently started app" is no longer possible on Android (≥ 5.0); today this is done with UsageStatsManager / accessibility events.
- Limitation: night-time "long sessions" partly artefacts of apps keeping the screen on (alarm clocks), which the authors admit; the title's "falling asleep" is not actually measured.
- Limitation: abstract says the average session is "less than a minute" but results report 71.56 s.

## How it relates to my thesis

Useful as a historical baseline and for method, not for current numbers. It already shows the pattern later called checking (oulasvirta2012) and micro-usage (ferreira2014): most sessions are one app and a few seconds, and communication apps open most sessions. The 30-second-gap session definition is one option for my logging (compare with vanberkel2016 on session gaps and andrews2015's ≤ 15 s "checks"). Night-time use of games and social apps links to the sleep findings (yang2020, chu2023). Comparing ~1 h/day in 2010 with ~4–5 h in 2015–2019 also illustrates the growth argued in olson2022.

## Quotes / figures worth citing (with page)

- "we find that the average session with an application lasts less than a minute, even though users spend almost an hour a day using their phones." (Abstract, p. 47)
- "the majority of sessions (68.2%) only contain a single application. In other words, people turn on their phone, use a single app, and put their phone back in standby." (p. 51)
- "for nearly half of all chains (49.60%) the first application belongs to the category Communication" (p. 52)
- Fig. 5: hourly share of launches by category. Fig. 9: transition probabilities between categories. Fig. 10: usage of specific apps by hour.
