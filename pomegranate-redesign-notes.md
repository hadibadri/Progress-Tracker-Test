# Pomegranate redesign: rationale (round 2)

**What this is.** This is a rebuild of the Pomegranate patient app for people on a weekly GLP-1 injection. Round 1 rebuilt the UX: one next step, the closed loop, the return after an absence, and calm paths for hard moments. In review, it still looked too much like the original: beige cards, bold sans and plum pills. Its logging screens were a keypad and forms, and it had a layout bug. **Round 2 keeps every flow, every line of copy and all the loop logic, and replaces the visual and motion layer** with two deliberately different worlds, instrument-style logging, the client's line-art figure as the brand's human signature, and a motion system that was checked frame by frame.

The working parts of the original are unchanged:

- the prescription-sourced dose in mg, mL and syringe units
- dose-day and late-dose logic taken from the label
- site rotation
- the 7-day average with a healthy-pace band
- waist and photo tracking
- the visit brief
- urgent signs with emergency numbers
- hide-weight mode
- the lock screen

## 0. What changed in round 2

| Area | Round 1 | Round 2 |
|---|---|---|
| Look | Beige cards, bold Plus Jakarta Sans, plum pills | Two worlds. **Light, Vessel-like editorial** for the functional core: sage and mist panels, a wavy edge into ivory, Geist Light display, Newsreader for small human sentences, Geist Mono corner labels. **Dark, Veri-like aura stages** for input and emotion: colour bleeds in from the edges into a dark centre. |
| Today hero | A misty headland photo with a figure crouching on the hillside, which the client found off-tone | **The client's own single-line figure**, vectorised faithfully, drawing itself on first open. The 7-day trend line passes behind her shoulder and ends in a frosted capsule with a chartreuse "now" dot. |
| Weight | A number keypad | A **tick ruler**. Drag it or flick it with inertia; it snaps to 0.1 with detents and a fixed chartreuse needle. It starts at last time's value and shows a dot-matrix readout that re-forms. "Type it" is the fallback. It is a `role=slider` with arrow, Page and Home/End keys and `aria-valuetext`. |
| Dose | A syringe drawing and a "Verify" button | **Press and hold a ring** on a rose-plum aura. It breathes while idle, fills tick by tick and blooms into jade with "Dose 10 recorded", plus Undo and Done. Keyboard Enter confirms. Releasing early unwinds it. |
| Side effects | Chips and a radio list | **Large tactile tiles** and a vertical **severity ruler** with a draggable knob. The aura deepens from lavender as severity rises. "Can't keep food or water down" switches on the flat clinical-alert panel. |
| Mood and energy | (none) | A new 10-second check-in: five colour orbs, and **the aura takes on the colour of the answer**. Choosing Low or Rough reveals a quiet offer to message Ana. |
| Onboarding | Four screens; "What to expect" sat behind the footer at 375×667 | The welcome, then four short steps on aura stages. **"What to expect" is its own step**: a vertical timeline you can scrub with a finger, arrow keys or taps, fully visible at 320×568, 375×667 and 393×852. |
| Closed loop | A static rail | The same four statuses, now with **a dot that travels along the line** to the current status. Nodes fill as it arrives. |
| Photography | Nine photos | Six atmospheric photos in which people are small in the frame. The hillside crouch, the sad figure at a window and an unused coast photo were removed. |

## 1. Retention: why people leave, where, and what helps

**Why they leave.**

- GLP-1 discontinuation reaches 64.8% within a year for people without diabetes (Rodriguez 2025, n=125,474).
- Moderate-to-severe GI events raise the risk of stopping (HR 1.19).
- Slow early progress raises it too: each 1% of weight lost cuts the hazard by 3.3%.
- Around these sit cost and access confusion (68% call cost a major barrier), onboarding friction, expectations broken in month two, and feeling unsupported.
- Two-thirds of patients hide their treatment, so anything public or loud is another reason to leave.

**Where they leave.** Health apps keep 3–8% of users at day 30. The drop points are:

1. account setup
2. the first injection
3. the first week of side effects
4. the first hard experience
5. month two, when the scale flattens

**What helps.**

- Human feedback is the only app add-on with a significant effect on weight in meta-analysis (−2.63 kg, Antoun 2022); feature count has no effect.
- Persistence on Wegovy and Zepbound rose from 33% to 61% between 2021 and 2024, and the authors credit dose management and side-effect management.
- Broken streaks demotivate people.
- In a 61,293-person megastudy, the best intervention rewarded coming back after a miss.

| Drop point | Designed moment |
|---|---|
| Account setup | A welcome, then four short steps: the plan, what to expect, the starting point and privacy. Every field is optional and Face ID comes last. Today is pre-selected as the dose day. |
| First injection | One next step on Today: "Your first dose. You've got this. 50 units". Then a hold-to-confirm ring that tells you how many units to draw, plus Needle tips. |
| First week | A week-one companion card and page: day 4 of 7, what most people notice, and that Ana checks in on day 3. |
| First hard experience | "Tell your care team" takes three taps from Today, Care or the hard-week card. The urgent route is always visible. |
| Month two | "Holding steady. Common in month two." This explains the step-shaped curve, shows what is still changing and sends the question to the visit brief. The dose stays the clinician's call. |

## 2. Five principles, screen by screen

| Screen | One obvious next action | Progress without judgement | Progressive disclosure | Beauty that serves comprehension | Support that feels real |
|---|---|---|---|---|---|
| **Today** | One pill-and-orb button for the next step ("Take today's dose") | A Newsreader status line, the trend crossing the hero and the capsule average. No streaks, and missed doses are never red. | At most one attention row, and two compact tiles (Trend, Care team) | The line-art figure, generous negative space, a dot-matrix-free calm number (50 units) | The Care-team tile shows live loop status with Ana and Dr. Shah |
| **Dose stage** | Press and hold the ring | Confirms the dose number ("Dose 10 recorded") and the next dose | Sites, missed-dose rules, needle tips and the vial check sit behind small links | Ring, needle and bloom; mg, mL and units as chips | The wrong-vial path stops the dose and messages the nurse |
| **Weight ruler** | Save | "0.6 lb less than last time" or "Same as last time", in neutral words. With hide-weight on, the trend is shown without the number. | Unit switch, and Type it | Dot-matrix readout and tick ruler | The 7-day average "does the judging" |
| **Progress** | Drag the capsule to read a day | Pace band, milestones at 5/10/15%, and a dose record that only grows | Weeks expand on tap; waist is a toggle | Sage panel, line crossing it, frosted capsule | Lab results carry Dr. Shah's note |
| **Care** | "Message your care team", or open the conversation | "No judgement" on the hard-week card | Brief, prescription and history in a list | Mist panel, travelling-dot loop | Reply-time promise, clinic number, 911 |
| **Onboarding** | One button per step | "Some weeks go up; that's usually water." | Waist, photo and hide-weight are optional | Aura stages and the figure on the welcome | Meet the prescriber and the nurse first |

## 3. The closed loop

A report or message becomes a conversation with four stations: **Sent → Delivered to care team → Nurse replied → Next step**.

- **Visible progress.** A dot travels along the line to the current station.
- **Honest copy at each step:**
  - "Sent at 9:41 am. We'll show you when it reaches your care team."
  - "Delivered to your care team at 9:42 am. Not read yet. Usually answered within 1 business day."
- **Next step from the care team.** It arrives as a sage card, for example "Try the nausea plan for three days. Keep your current dose; Dr. Shah will review it at your visit."
- **Urgent route.** Every thread ends with "call the clinic on (555) 010-0142, or 911".
- **Escalation.** "I can't keep food or water down" or any urgent sign opens the flat clinical-alert screen. Today keeps an alert card until the patient taps "I've spoken to the clinic".
- **No dose advice.** The app never advises a dose change.

In the demo, delivery happens automatically after about 2 s. Replies and next steps are advanced from the reviewer panel or the long-press demo menu.

## 4. Designing for the return

After 7 or more days away, Today becomes a calm aura stage.

1. A lavender **fog lifts**.
2. The client's figure, mirrored, draws itself beside "**Welcome back, Denise.** It's good to see you. There's nothing to catch up on."
3. "**Your record is safe**": the seed record keeps missed weeks as soft outlines, never as a reset.
4. **One next step:** "Your next dose is tomorrow, Wednesday", with **Remind me tomorrow morning** and **Ask Ana first**.
5. An optional "**Did something get in the way?**" where each chip routes to the right help: side effects, cost or refills, life got busy, feeling low (with 988), or results felt slow.
6. **Go to Today.**

There are no red badges and no backlog.

## 5. Visual system: two worlds

**Light, editorial (Today, Progress, Care, messages, information pages).** Warm ivory (#F4EEE6) and paper, with panels in sage (#B9CCBD) and mist (#E4D7E1). A wavy edge leads into the page.

- **Type:** **Geist 300** at 27–40 px with −3.5 to −4.5% tracking for display, and 400/500 for interface text. **Newsreader** is used for the small human sentences, and **Geist Mono** for corner-pinned micro labels set as a left/right pair.
- **Primary action:** a dark pill with a white orb.
- **Surfaces:** cards are paper with no borders. Glass is used only on the frosted capsule, the avatar square and the tab bar.

**Dark aura stages (all input and emotional moments).** The base is #141315. Colour bleeds in from the corners and the bottom edge into a dark radial core:

- **Rare Jade #A6CFB8** means progress: weight, protein, workouts and milestones.
- **Tranquil Lavender #D0A8C9 and mauve** mean calm and support: side effects, the return and feeling low.
- **Dusty rose (#D9A3A0) to muted plum (#8A4A6B)** means dose and treatment. It is softer than Floral Magenta, as the brief asked.

Text sits on smoked glass (#141315 at 50–80%), so every label passes AA over the glow.

**The one chartreuse accent (#E7FE55)** marks "where you are now" and nothing else: the ruler needle, the hold-ring needle, the capsule's now-dot, the timeline needle, the severity knob's core, the loop's travelling dot and today's bar. Its sharpness carries meaning, which is why it is never used as decoration.

**The clinical alert has its own treatment.** It is the only flat, hard-edged (4–8 px radius), glow-free surface in the app, in oxblood #7A1527 with ivory type. No aura ever uses it, so it can't be mistaken for mood.

**Dot-matrix numerals** are a custom 5×7 SVG grid that morphs dot by dot. They are used only for hero numbers: the weight readout, the units on the dose disc, protein grams, workout minutes and the milestone percentage.

**The line-art figure is the human signature.** It is the client's own drawing. It was traced with potrace at 3× supersampling, and the vector was compared with the PNG by overlay: 100% of ink within 1 px either way, IoU 0.96 and a mean difference of 0.34/255. Nothing was redrawn or simplified. It is recoloured to plum-ink on the sage panel and to ivory on dark stages. It appears four times, each with a different crop, and never twice on one screen:

- the full figure on Today
- head and shoulders on the onboarding welcome
- head and shoulders, mirrored, on the return
- the face only on the milestone

The milestone uses the face only on purpose: at a weight milestone we avoid presenting a body as the achievement.

**Photography.** Six atmospheric photos (Open Images, CC BY 2.0, graded to the palette) in which people are small in a big, quiet space:

- two walkers for week one
- a misty path for month two
- footprints for the record
- a beach in fog for photos
- a jetty at dusk for hard weeks
- a hazy shore for the share card

## 6. Motion specification

**Rules:**

- Animate transform and opacity only, with three exceptions:
  - the line-art reveal, which animates `stroke-dashoffset` on its mask (the brief asked for exactly this)
  - the dot-matrix digits
  - the hold-ring ticks

  The last two animate opacity and transform on SVG children, which repaint on the main thread. All three were measured under throttling (section 7).
- Springs are real damped springs sampled into CSS `linear()`:
  - **--spring** k=180, c=19: about 560 ms with a little overshoot, used for presses, pills and pops.
  - **--spring-soft** k=110, c=17: about 750 ms, gentle, used for sheets, pages and rises.
  - **--spring-snap** k=320, c=30.
- Instruments use a JS spring (k=300, c=32) that carries the release velocity.
- `--out` is cubic-bezier(.16,1,.3,1).
- **Reduced motion:** nothing moves. Pages cross-fade in 0.25 s, auras stand still, the figure is shown already drawn, digits change by opacity only and the fog is removed. The dose still requires a 1.15 s hold, because the hold is a deliberate confirmation, not an animation.

| # | Interaction | Choreography | Duration and easing |
|---|---|---|---|
| 1 | **Today, first open** | The figure draws through seven mask strokes in pen order: profile, eye, hair, back, spine, waist, hip. A full-mask fade then guarantees every hairline is present. The ivory glow fades in and then breathes. The trend line reveals left to right, behind her shoulder. The capsule rises, the now-dot pops and the labels fade in. The greeting and cards rise in sequence. | Strokes 0.15–2.0 s, each cubic-bezier(.42,.02,.18,1). Mask fade 0.6 s at about 2.0 s. Glow 1.6 s, then breathes over 8 s alternate (translate −3%/2%, scale 1.07). Line 1.5 s cubic-bezier(.65,0,.35,1) at 0.26 s. Capsule 1 s --spring at 1.25 s. Dot 0.8 s at 1.55 s. Rises 0.9 s --spring-soft, 80 ms stagger. |
| 2 | **Tab switch (shared-element morph)** | The coloured hero panel travels as a FLIP ghost from the old tab's shape and colour to the new one (sage to sage, or sage to mist). The old content fades through and the new content rises 10 px. The tab pill slides. Progress redraws its line. | Panel 0.62 s --spring-soft, colour 0.38 s. Old content 0.15 s ease-in. New content 0.34 s --out at 0.1 s. Pill 0.62 s --spring. Line 0.7 s. |
| 3 | **Page push and back** | The page slides in from the right while the view behind parallaxes 14% left. Edge-swipe follows the finger. | 0.62 s --spring-soft in, 0.42 s cubic-bezier(.4,0,.2,1) out. Dismisses past 35% of the width or above 650 px/s. |
| 4 | **Sheet** | The sheet springs up while the view behind scales to 0.94 and the scrim fades. Drag the grabber to dismiss. | 0.66 s --spring-soft, 0.45 s scrim. Dismisses past 110 px or above 700 px/s. |
| 5 | **Aura stage entrance** | The dark ground arrives fast, then the core contracts from 1.5 to 1 so colour blooms in from the edges. Content rises in sequence; the footer comes last. | Ground 0.26 s cubic-bezier(.2,0,0,1). Core 1.4 s --spring-soft. Rises 0.75 s from 0.1 s, 60 ms stagger. Exit fades 0.38 s. |
| 6 | **Aura idle** | Three glow fields drift; palette changes cross-fade. | 9 s ease-in-out alternate; 1 s cross-fade. |
| 7 | **Weight ruler** | Follows the finger 1:1 (90 px = 1 lb, one update per frame). A flick glides with exponential decay, then springs into the nearest 0.1 detent. Each 0.1 gives a 2 ms haptic; each whole pound gives a 7 ms haptic and a needle pulse. | Decay 0.9962/ms. Snap spring k=300, c=32 with release velocity. Needle pulse 0.2 s. |
| 8 | **Dot-matrix digits** | Each dot fades and scales between lit and ghost, top row first, glyph by glyph, with a little randomness, so the number re-forms rather than flips. While dragging, digits update instantly. | 0.26 s opacity and 0.55 s --spring scale. Delay is 22 ms × row + 8 ms × column + 24 ms × glyph + up to 24 ms random. |
| 9 | **Dose hold** | Idle: the ring breathes. While holding: 72 ticks light in sequence behind a rotating chartreuse needle, and the disc sinks. Early release: the ticks go out in reverse and the needle springs home. Completion: the aura blooms (the core contracts and recovers) and the palette turns from rose to jade. The disc pops, "50" re-forms into a tick, the title swaps, the sites fade and Undo/Done rise. | Hold 1.15 s; ticks 0.12 s each, delay i × 1.15 s / 72. Needle rotation is linear. Breath 4.4 s. Bloom 2 s --out. Pop 0.8 s --spring. Footer 0.7 s at 0.65 s. |
| 10 | **Closed-loop dot** | The dot travels from the previous station to the new one and the line fills behind it. Each node fills as the dot arrives. On open, the dot travels from Sent to the current station. | 1–1.1 s --spring-soft. Nodes fill at about 180 ms + 620 ms per step. |
| 11 | **Severity ruler** | The knob springs to the chosen level, or follows the finger and snaps. The fill grows, and the aura deepens at "Quite a lot". | 0.6 s --spring; fill 0.6 s --spring-soft; aura 1 s. |
| 12 | **Tiles and chips** | On press they sink 1.5 px and scale to 0.95–0.97, and their shadow layer fades (depth). When selected, a fill grows from 0.82 and a tick pops. | 0.45 s --spring; fill 0.5 s --spring with 0.22 s opacity. |
| 13 | **Mood** | The chosen orb grows to 1.16 with a halo. The stage cross-fades to that mood's palette and the note rises. | 0.55 s --spring; 1 s palette. |
| 14 | **Milestone** | The jade aura blooms. The ivory face draws. Dots fly in from scattered positions and assemble "5%", row by row. The text rises. | Dots: 1.2 s --spring transform and 0.7 s opacity, staggered 40 ms per row, 90 ms per glyph, plus up to 160 ms random. Figure 0.2–1.2 s. Text from 0.5 s. |
| 15 | **Return fog-lift** | A lavender fog with drifting light lifts and thins. The header fades in, the content rises, and the mirrored figure draws. | Fog 1.7 s cubic-bezier(.65,0,.35,1) at 0.12 s. Content from 0.62 s, 90 ms stagger. Figure from 0.85 s. |
| 16 | **Onboarding** | Each step's content rises in sequence while the aura's palette shifts. The timeline needle follows the finger, snaps to the nearest stage, and the fill grows. The welcome figure draws. | 0.85 s --spring-soft, 80 ms stagger. Needle 0.7 s --spring. Figure 0.35–1.5 s. |
| 17 | **Toast** | Rises 24 px from 0.97 scale; Undo is always in reach. | 0.55 s --spring; 0.25 s opacity. |
| 18 | **Toggles and segments** | The knob slides and the fill cross-fades; the segment thumb glides. | 0.5 s / 0.55 s --spring. |
| 19 | **Launch and lock** | The aura core settles from 1.7 and the wordmark rises. Unlock fades and scales away. | 1.4 s --out; 0.5 s. |

## 7. Verification

All checks ran in Playwright on Chromium. Viewports were 393×852, 375×667 and 320×568, plus a 1440×900 desktop frame.

**Static checks.** These ran over 56 states and flows at all three sizes: 168 screens and about 2,800 text runs.

- **Contrast** was measured against the actual pixels behind each text run, including over auras, glass, the figure and photos. Result: 0 AA failures.
- **Touch targets:** 0 under 44 px.
- **Horizontal overflow:** 0.
- **Console errors:** 0.
- **Occlusion (new):** for every text run and control, the check computes whether it can be scrolled fully into the visible band. That band excludes any fixed, sticky or overlaying element, such as the floating tab bar, footers or headers. It also flags any line that sits sliced in half at rest by a scroll edge or footer, unless that edge carries the "more below" fade. Result: 0 occluded, 0 sliced.
- **Fit:** the welcome and "What to expect" steps must fit without scrolling at every size; the other onboarding steps, the dose stage and the milestone must fit from 375×667 up. Result: 0 failures.
- **Validation:** run against the round-1 build, the occlusion check flags exactly the reported bug: "What to expect" was sliced at 514–537 px against a footer edge at 525 px.

**Crawl.** Every visible control was tapped at all three sizes, 420 per size. At each size:

- 376 changed the UI
- 10 long-presses opened the demo menu
- 2 press-and-holds recorded a dose
- 22 were already in their selected state
- 7 were phone links
- 1 opened the file chooser
- 1 was the capsule tapped at the point it already shows
- 1 was reported as a no-op. This is a test artefact: the wordmark had scrolled off-screen in a pre-scrolled flow.

**End to end.** 61 of 61 checks pass:

- onboarding, including scrubbing and the timeline arrow keys
- the ruler by keyboard (0.1 and 1.0 steps), by drag and snap, and by flick with inertia, plus the typed fallback
- dose: early release does nothing, holding records, Undo in the stage and in the toast, and keyboard Enter confirms
- the severity ruler by drag
- the full loop with the travelling dot
- persistence across a reload
- mood colour shifts and the protein readout
- the return, including fog, scrolling and the reminder
- the plateau explainer feeding the brief
- the urgent route, which is flat with no aura
- milestone dots assembling
- hide-weight
- the demo menu
- the line art: drawn on first open, complete at rest, and already drawn under reduced motion

**Motion.** Each of 21 interactions was captured as composited frames with the CDP screencast (about 40–280 frames each). Each has a contact sheet in `screenshots/motion/`, including a dedicated draw-on frame strip for the line-art hero. The frames were checked automatically:

- **Flashes:** a frame whose luminance jumps away from both its neighbours. Result: 0.
- **Snaps:** more than 35% of the screen changing in a single frame with stable frames either side. The only snaps found are the deliberate demo state switches, which hard-cut by design.
- **End state:** the last frame compared with a settled screenshot. Result: within 0.33/255 for every interaction.

The frames were also reviewed by eye. Problems found and fixed during the passes:

- **Stage entry:** a double exposure of the light Today showing through the stage. Fixed with a fast dark ground before the content rises.
- **Tab bar:** the active pill covered its own label during the switch.
- **View Transitions version of the tab morph:** it froze for about 230 ms, flashed the body blank after the switch, and stalled with 15–17 long frames under 4× CPU. It was replaced by the FLIP ghost-panel morph.
- **Ruler:** dot updates during drags were heavy. Fixed by making digits update instantly while dragging and coalescing pointer moves.
- **Aura glass:** backdrop blur sat over animated glows. Removed.
- **Glow drift:** the drifting glows were changed from scale to translate.

**Performance.** Each interaction was re-run under **4× CPU throttling** while logging rAF frame times and Long Animation Frames:

Across 20 interactions, 18 hold a 95th-percentile frame time of 16.8 ms or better under 4× CPU, and 87 of 3499 frames (2.5%) ran over 16.7 ms. Most of those long frames fall on the tap itself, when the next stage is built. The worst frames come from opening a stage or tab, where page construction lands in the tap's frame before the compositor-driven transition starts. Fixes from earlier passes: dot-matrix dots became compositor-driven HTML dots; the keyboard steps on the ruler re-form the digits once on settle; only lit milestone dots fly; and the tab morph is a FLIP ghost instead of a View Transition.

| Interaction | Composited frames | Flashes | Snaps | End-state diff (/255) | 4× CPU p95 | 4× frames over 16.7 ms | 4× worst frame |
|---|---|---|---|---|---|---|---|
| Today, first open | 197 | 0 | 0 | 0.05 | 16.8 ms | 1 of 250 | 16.8 ms |
| Onboarding welcome | 166 | 0 | 1 (demo state switch) | 0.03 | 16.8 ms | 2 of 216 | 16.8 ms |
| Weight ruler | 173 | 0 | 0 | 0.06 | 16.8 ms | 7 of 219 | 33.4 ms |
| Dot-matrix digits re-forming (keyboard steps on the ruler) | 125 | 0 | 0 | 0.05 | 16.8 ms | 6 of 149 | 33.4 ms |
| Dose: press-and-hold ring and bloom | 244 | 0 | 0 | 0.05 | 16.8 ms | 7 of 330 | 66.6 ms |
| Dose: early release unwinds the ring | 121 | 0 | 0 | 0.13 | 16.8 ms | 7 of 151 | 49.9 ms |
| Closed loop | 111 | 0 | 0 | 0.0 | 16.8 ms | 1 of 140 | 16.8 ms |
| Milestone | 161 | 0 | 0 | 0.05 | 16.8 ms | 10 of 217 | 66.7 ms |
| Return after 10 days | 194 | 0 | 1 (demo state switch) | 0.04 | 16.8 ms | 1 of 274 | 16.8 ms |
| Tab switch (hero, trend, active pill) | 53 | 0 | 0 | 0.0 | 33.3 ms | 6 of 118 | 233.3 ms |
| Tab switch to Care | 40 | 0 | 0 | 0.0 | 16.8 ms | 3 of 110 | 133.3 ms |
| Spring sheet | 42 | 0 | 0 | 0.0 | 16.8 ms | 2 of 112 | 66.6 ms |
| Sheet drag to dismiss | 48 | 0 | 0 | 0.0 | 16.8 ms | 2 of 117 | 50 ms |
| Tactile tiles and chips pressing with depth | 136 | 0 | 0 | 0.05 | 16.8 ms | 6 of 167 | 66.7 ms |
| Severity ruler | 118 | 0 | 0 | 0.03 | 16.7 ms | 3 of 169 | 33.4 ms |
| Aura stage entrance | 74 | 0 | 0 | 0.33 | 16.8 ms | 4 of 98 | 33.3 ms |
| Mood | 161 | 0 | 0 | 0.05 | 16.8 ms | 3 of 214 | 33.4 ms |
| Onboarding | 96 | 0 | 0 | 0.03 | 33.3 ms | 10 of 149 | 50 ms |
| Light page push and back (parallax) | 77 | 0 | 0 | 0.0 | 16.7 ms | 3 of 197 | 83.2 ms |
| Toast springs in with Undo | 83 | 0 | 0 | 0.05 | 16.8 ms | 3 of 102 | 116.7 ms |

## 8. Open items

- **Line-art licence.** The figure was supplied by the client with no licence information. It is listed as "Supplied by the client — licence to be confirmed", and it looks like a stock vector, so confirm the licence before release.
- **More line art needed.** No further line-art sources could be reached: Openverse, Wikimedia, SVG Repo, rawpixel, Vecteezy and Freepik were all blocked by the network. The onboarding welcome, return and milestone therefore reuse the client's drawing in different crops. Each needs its own drawing in the same hand: head and shoulders (welcome), a figure turning back (return), and a lifted face (milestone).
- **Photos.** Open Images photos (CC BY 2.0) carry no model releases, so re-license or re-shoot them before launch. The wordmark is a Bodoni Moda stand-in.
- **Simulated workflow.** The care-team workflow is simulated. Real staffing has to back the "1 business day" promise.
- **Fictional details.** The nurse, the doctor, the clinic number and the pharmacy are all fictional.
- **Sign-off.** Clinical copy needs clinical and legal sign-off.
- **Performance caveat.** The rAF and Long Animation Frame figures come from software-rendered headless Chromium. Confirm them on a mid-range Android phone.
