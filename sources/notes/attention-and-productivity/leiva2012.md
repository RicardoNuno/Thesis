# leiva2012: Back to the app: the costs of mobile application interruptions

**Authors / venue / year:** Leiva, Böhmer, Gehring & Krüger / MobileHCI '12, 291–294 (short paper) / 2012
**Link:** https://doi.org/10.1145/2371574.2371617 (copy: https://interruptions.net/literature/Leiva-MobileHCI12.pdf)
**Relevance:** low

## Summary (3 sentences)

Mined the AppSensor dataset (bohmer2011: 3,611 Android users worldwide, Aug 2010–Jan 2012) to detect when an app was left for another app or an incoming call and then resumed. These interruptions are rare (about 3% of daily usage for calls, 8% for app switching), but when they happen the interrupted app takes much longer to finish, up to four times its normal runtime. Proposes preventive (warn before interrupting) and curative (help regain context) design strategies.

## Method

- AppSensor: background Android service sampling the foreground app at 2 Hz; 5.5M samples, 15,756 apps, 3,611 users, 532 days.
- Interruption = foreground goes app x → y → back to x. "Internal" = user switches app on purpose; "external" = incoming phone call. Launcher and dialler excluded as interrupted apps.
- Overhead (resumption lag) = runtime when interrupted − normal runtime of the same app for the same user (paired cases only).
- Non-parametric tests (Kolmogorov–Smirnov), macro-averaged per user.

## Results / evidence

- Interruptions as % of daily usage: calls 3.2%, app switching 8.3%.
- Normal runtime ~19–25 s vs ~88–107 s when interrupted; overhead ~34 s (internal) and ~43 s (external).
- Calls are shorter than app-switch interruptions (12.5 s vs 23.7 s) but cause more overhead → external interruptions are more disruptive.
- Interrupted runtime "could be increased by up to four times".
- Design ideas: delay the call screen ~500 ms with a signal so the user can save their mental state; overlay instead of full screen; replay the last interactions or leave a visual cue on return.

## Strengths / limitations

- Strength: very large in-the-wild logged dataset; simple, reusable detection of interruptions from foreground-app logs.
- Limitation: **dated**: data from 2010–2012 (early Android, before Instagram/Snapchat/TikTok dominance, modern notifications and app-switching gestures); usage patterns have changed a lot.
- Limitation: notifications are not studied; "external" means phone calls only, and self-initiated checks are not separated.
- Limitation: treats app runtime as task completion time; no idea what the task was, and longer runtime after returning is not necessarily a cost.
- Limitation: uncontrolled data mining; short 4-page paper; effect sizes small for the call vs switch differences (d ≈ 0.2).

## How it relates to my thesis

Mostly a historical / methodological reference. Useful as an early example of detecting interruptions purely from foreground-app logs (what I would get from UsageStatsManager today), and as the source of the "up to 4×" figure quoted by wilmer2017 (which reports it as "400%"). Its findings about interruption frequency should not be cited as current; for today's numbers use heitmayer2021 and pielot2014 (notifications) instead.

## Quotes / figures worth citing (with page)

- "Our findings reveal that these interruptions rarely happen (at most 10% of the daily application usage), but when they do, they may introduce a significant overhead (can delay completion of a task by up to 4 times)." (Abstract, p. 291)
- "Application interruptions rarely happen on smartphones, but when they do, they can be really costly for the user." (p. 294)
- Table 3 (p. 293): interruption frequency, runtime and overhead, internal vs external.
