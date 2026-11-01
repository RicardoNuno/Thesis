# datta2022: Mind-proofing Your Phone: Navigating the Digital Minefield with GreaseTerminator

**Authors / venue / year:** Datta, Kollnig & Shadbolt / IUI '22, 523–536 / 2022
**Link:** https://doi.org/10.1145/3490099.3511152 (preprint: https://arxiv.org/abs/2112.10699; code: https://github.com/greaseuniverse/greaseterminator)
**Relevance:** medium

_Read from the arXiv v3 preprint (Feb 2022); quotes cite sections._

## Summary (3 sentences)

A research framework for Android that intervenes at the interface level: the phone's screen is streamed over ADB to a PC server, which detects elements with OCR, template matching or ML models and sends back graphics drawn on a transparent overlay ("draw over other apps"). Three "hooks" (text, mask, model) let researchers build interventions that work across apps, browsers and the home screen without modifying app code or rooting the phone. Five case studies show it working: hiding the stories bar, fading the screen after excessive scrolling, hiding like/share counts, blacking out hate speech, and censoring nudity; there is no user study.

## Method

- Review of six ways to change app behaviour on phones (see the next section), from which two requirements are derived: interface-orientation and ease of use.
- Architecture: Android app streams the screen to a server via ADB; Python hooks process frames; overlay rendered back on the device after the overlay permission is granted.
  - Text hook: EAST text detection + Tesseract OCR.
  - Mask hook: multi-scale template matching against cropped screenshots (contours for dynamic elements), then majority-colour inpainting.
  - Model hook: any ML model on the frame.
- Latency: ADB relay ~50 ms vs ~800 ms with ScreenCast over TCP/UDP; on-device inference in a Linux container took 60–120 s per frame. Server had 4× RTX 2080.
- Evaluation: five case studies described as Problem / Known implementations / Challenges / Implementation with GreaseTerminator, loosely based on cognitive walkthroughs.

## Types of app modification (§3.1–3.2)

1. **App-external modifications**: a separate app affects other apps without changing them or the OS; uninstalling it restores everything. The most common approach: tracking usage time, notifications during use (timers, warnings), blocking actions. Examples: HabitLab, AppDetox, NUGU, MyTime, okeke2018. Easy for users and on the Play Store, but limited to what the OS exposes, so it acts on whole apps rather than elements inside them.
2. **App pre-install modifications**: the app's code is changed before installation, then the patched app is installed. Examples: AppGuard (privacy), GreaseDroid (removing dark patterns with community patches), Lucky Patcher (removing payment code). Can change anything inside an app, but needs sideloading, high developer expertise, and patches break with app updates and differ per app.
3. **OS-level modifications**: root access to change the OS and apps. Examples: Xposed (Android), Cydia Substrate (iOS jailbreak), TaintDroid, ProtectMyPrivacy. Most powerful, but users must root the phone (may void warranty), tools are often not on the Play Store, and development requires low-level Android knowledge.
4. **Virtual environment modifications**: a virtual space on the phone simulates root so other modification tools can run without rooting. Example: VirtualXposed. Avoids rooting, but every app the user wants modified must run inside the virtual environment, and it is as hard to develop for as the OS-level approach.
5. **Browser modifications**: scripts change a website's client-side code in a mobile browser, ported from desktop tools. Examples: TamperMonkey, OilCan, Swipe for Facebook. Easy to develop (JavaScript) and use, but only works on websites, not inside native apps.
6. **Visual overlay modifications**: graphics are drawn on a layer above whatever is on screen (apps, browser, video, home screen); purely visual, functionality underneath is unchanged. Examples: GreaseTerminator, DetoxDroid, Gray-Switch, Google Accessibility Suite. Works across apps with only the overlay permission, but it has to know what is on screen (here via screen capture) and cannot change app behaviour.

General barriers named by the authors: (i) developers must build each intervention and keep it working across 2.9 million apps and their updates, and port it between platforms; (ii) users face set-up cost for each separate tool and juggling many of them. Interventions that remove elements outright can also block wanted functionality, and HabitLab users weakened or uninstalled interventions over time.

## Results / evidence

- Element occlusion: one screenshot of a stories bar (row of circles) hides it in Twitter and LinkedIn, and may survive app updates and work in browsers.
- Usage locking: detects scrolling by comparing frames and raises the opacity of a white mask as scrolling or time continues (like Anchor on desktop).
- Demetrification: hides like/share counts in Facebook, Twitter and Instagram from one mask per app.
- Hate speech and nudity filters work but visibly overblock (Figs. 8–9).
- Screen updates every ~50 ms, "hardly noticeable"; battery not measured.

## Strengths / limitations

- Strength: clear survey of Android modification approaches and their trade-offs; open-source code.
- Strength: interface-level detection is app-agnostic, so one intervention can cover many apps and the browser.
- Limitation: no evaluation with users or developers; "ease of use" is the authors' own walkthrough.
- Limitation: needs a PC server and an ADB connection, so it works in a lab or at home, not in daily mobile use; offline use is impossible.
- Limitation: the whole screen is streamed to a server, a serious privacy risk the authors acknowledge (data or password theft by intervention developers).
- Limitation: says it needs "no privilege escalation", but screen capture over ADB is a developer-level grant, which the paper does not discuss.
- Limitation: battery impact of continuous streaming is mentioned but not measured; the 5 ms latency figure is theoretical and its arithmetic does not match the stated ~1 Mb image size.

## How it relates to my thesis

Useful mainly as a map of the technical options on Android (overlay, Accessibility, root, patching, browser scripts) and as an example of the overlay permission used for interventions inside apps. It shows the opposite end from a lightweight, consent-friendly prototype: powerful and app-agnostic, but with constant screen capture, a server, and unknown battery cost, which are the costs my evaluation criteria (battery, acceptability, privacy) would penalise. Its feature-level interventions (hiding stories, fading after scrolling) contrast with app-level time limits like Digital Wellbeing and okeke2018, and the gradual fade is another friction design to compare with haliburton2024. Its discussion of paternalism versus autonomy echoes kim2017pomodolock and lyngs2019 on user control.

## Quotes / figures worth citing (with section)

- "The last line of defense against a range of digital harms ... is the user interface." (Abstract)
- "The usage of GreaseTerminator requires no privilege escalation or root access; the end-user only needs to accept permissions to draw over other apps." (§7.2)
- "Continuously streaming the screen may affect battery life as well." (§7.3)
- "Intervention developers can make use of interventions and screen streaming to steal data or passwords from the end-user." (§7.3)
- "In the case of HabitLab, users uninstalled or weakened the extent of interventions over time, possibly due to the intrusive nature of the tool" (§3.2)
- Fig. 1: architecture. Table 1: interventions, hooks and harms. Figs. 5–7: stories bar removal, scroll fade, demetrification.
