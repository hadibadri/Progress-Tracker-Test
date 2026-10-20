# Why switch to Pomegranate, and why stay

**Switching, identity and the concept prototype.** 20 October 2026. Written for the founder and the design team.

This report builds on the client's own research, [Pomegranate_progress_tracker_research.md](./Pomegranate_progress_tracker_research.md) ("the client research"), without repeating it. It also draws on a review of the current HTML concept, the round-2 design notes and the 393×852 screenshots. Four changes to the prototype are being built now and are treated here as in progress: a Denise/Joe persona switch, a Wrapped-style chapter recap with a privacy-safe share card, light-theme keypad-first logging, and removal of the dot-matrix digits. Each section separates **Evidence**, which is what sources show, from **Call**, which is our judgement.

---

## The answer on one page

1. **Pomegranate can't win by out-featuring Shotsy, MyFitnessPal or Oura. It wins by being the only app whose data is true.** Once a dose changes, a pharmacy changes the vial strength, or a refill ships, every consumer tracker is out of date. Pomegranate is the only app that already knows. Those moments are the switching triggers, and Pomegranate controls them.
2. **Switching costs in this category are mostly emotional and habitual, not technical.** In the standard typology, relational costs (identity and bonds) predict staying more strongly than procedural or financial ones ([Burnham, Frels & Mahajan 2003](https://journals.sagepub.com/doi/10.1177/0092070302250897); replications are mixed). Pomegranate should make procedural cost close to zero with "Bring your history", and earn a *legitimate* relational cost: a named nurse who answers.
3. **The first five minutes must show a richer history than the old app, with nothing typed.** That means the prescription, the vial strength in syringe units, the next dose, the price and the care team, plus months of past weights from Apple Health with dose steps drawn on the line.
4. **The best "tell a friend" moment is "my log changed my care."** Ranked next are the new-vial-strength catch, the return after absence that tells you whether you can restart, and the brief your doctor had already read. The prototype has most of the machinery but rarely shows the outcome in one sentence.
5. **The visual identity is currently borrowed.** It takes the chartreuse needle, tick rulers, dark aura stages (even the palette names "Rare Jade" and "Tranquil Lavender") and dot-matrix numerals from Ron Design Lab's Veri case. The frosted capsule over a trend line crossing a person, and the wavy panel edge, come from the Vessel case. The line-art figure is a stock genre. **None of the client's brand colours (#861A26, #660C21, #841839, #1B414A) appear in the prototype.** The only oxblood is the urgent-alert colour, so the brand's own colour currently means "something is wrong."
6. **The ownable system is the inside of the fruit, used as a data structure rather than decoration.** One seed is one treatment week. One chamber is one chapter of care (each dose step, then maintenance). The record only grows, and gaps stay as soft outlines. It works on Today, at dose confirmation, at a chapter close, on the return and on a share card that shows no numbers.
7. **Readability is a first-class mode, not a setting buried in a menu.** The patients are 35–60, and most need reading glasses by 45. The prototype sets labels at 9.5–12 px in uppercase monospace and uses 12.5 px serif italics. A "Clear text" mode, offered in onboarding and following the phone's text size, is a must for the concept.
8. **Publish promises that can be checked.** Name the reply time, no ads, no data selling, no upsells, care never gated on app use, history always exportable, and no surprise charges. These are what this audience rewards. Upsells, hallucinating AI and data sales are what it punishes.

---

## Method and limits

Sources are 2025–2026 news, store-listing data, vendor help pages, peer-reviewed studies and the client's 2,300-post Reddit dataset. **Several sites could not be fetched through the network proxy**: shotsyapp.com, withings.com, mdlinx.com, businesswire.com and developer.apple.com page bodies. For those, we relied on search-result snippets and say so where it matters. Many "switching" articles in 2026 are written by competitors (MyNetDiary, Nutrola, Fitia, GLP3 Planner, unstar.app), and they are flagged where cited. Store reviews and Reddit posts are anecdotes, not prevalence.

---

## 1. Why people stay with apps they trust

### Evidence

| Lock-in force | What the evidence shows | Strength in GLP-1 tracking |
|---|---|---|
| **Accumulated history** | MFP's April 2026 redesign (v26.16.0) replaced the Diary, offered no way back, and its rating fell sharply ([MWM](https://mwm.ai/articles/myfitnesspal-v26-16-0-replaces-diary-with-new-ui-sparking-rating-drop-in-april-2026)). The harshest reviews came from users with years of logs ([MyNetDiary, competitor](https://www.mynetdiary.com/diet-app-scorecard-april-2026.html)). History keeps them "miserable rather than gone" ([1vm9rxh](https://redd.it/1vm9rxh)). | **Medium.** Shotsy stores data on-device and in iCloud ([App Store](https://apps.apple.com/us/app/-/id6499510249)). |
| **Sunk effort** | People overvalue what they built ([Norton et al. 2012](https://doi.org/10.1016/j.jcps.2011.08.002)). An MFP change that ended a 796-day streak felt like a loss ([1steb4o](https://redd.it/1steb4o)). | **Medium.** Weekly shots build a shorter history than daily food logs. |
| **Habit anchored to a cue** | Shotsy sells dose-day countdowns and alerts ([App Store](https://apps.apple.com/us/app/-/id6499510249)). | **High.** Whoever owns dose-day morning owns the habit. |
| **Identity and affect** | Shotsy: 4.8★, praised for "no data harvesting" (client research). | **High.** Its privacy stance is part of who its users are. |
| **Hardware and integrations** | Oura launched GLP-1 Insights and a LillyDirect partnership in June 2026 ([HLTH](https://hlth.com/insights/news/oura-and-lillydirect-partner-to-support-glp-1-users-with-wearable-insights-and-care-tools)). | **High for owners.** Read from these devices; don't compete with them. |
| **Social graph** | Strava and Hevy hold people through followers. Nobody shares medication (client research). | **Low.** Treatment is hidden, so there is no graph to lose. |
| **Procedural cost** | In a 218-person study, procedural cost had **no significant effect** on switching intention; dissatisfaction, alternatives and habit did ([NTU](https://review.management.ntu.edu.tw/paper/10859-P.pdf)). | A reason to move matters more than the effort of moving. |

### Call

GLP-1 patients have little lock-in: Shotsy is the only tracker named in 800 GLP-1 posts, and only 3 times (client research). What holds them is the dose-day habit, a modest history and trust in Shotsy's privacy. Relational costs predict staying most strongly ([Burnham et al. 2003](https://journals.sagepub.com/doi/10.1177/0092070302250897)). So Pomegranate should:

- **Take over the cue, not the app.** Its dose-day reminder carries the right units for *this* vial.
- **Absorb the history**, so nothing is lost.
- **Match Shotsy's privacy stance publicly**, and exceed it.
- **Build the bond with a real person.** It is the one fair switching cost: patients stay because Ana answers, not because their data is trapped.

---

## 2. What makes people switch: the trigger moments

### Evidence from 2025–2026

| Trigger | Concrete story (2025–2026) | Source |
|---|---|---|
| **Redesign or removed feature** | MFP v26.16.0 (21 April 2026) removed copying single foods; rating collapsed; competitors report moves to MacroFactor, Cronometer, Lose It. | [MWM](https://mwm.ai/articles/myfitnesspal-v26-16-0-replaces-diary-with-new-ui-sparking-rating-drop-in-april-2026); [Fitia, competitor](https://fitia.app/learn/article/best-myfitnesspal-alternatives-2026/) |
| **Retroactive fee** | WHOOP charged members $49–$79 to upgrade (May 2025), deleted a "free upgrade" promise, then partly reversed. | [TechRadar](https://www.techradar.com/health-fitness/fitness-trackers/whoop-has-broken-a-promise-on-free-hardware-upgrades-and-users-arent-pleased) |
| **Hostility to your data** | Strava sued Garmin over API terms (Oct 2025) and dropped it 21 days later after uproar. | [BikeRadar](https://www.bikeradar.com/news/strava-drops-lawsuit-against-garmin-21-days-after-filing-it) |
| **Forced migration** | Fitbit accounts had to move to Google by 19 May 2026; unmigrated data was due for deletion on 15 July. | [9to5Google](https://9to5google.com/2026/01/31/fitbit-google-account-may-2026-deadline/) |
| **Privacy scandal** | After 23andMe's bankruptcy, about 1.9M customers (around 15%) asked for deletion. | [Business Insider via Yahoo](https://www.yahoo.com/news/almost-2-million-23andme-users-094501555.html) |
| **Medication continuity broken** | Novo ended its Hims partnership (June 2025). Hims launched and pulled a compounded pill within two days (Feb 2026). | [GMA](https://www.goodmorningamerica.com/wellness/story/novo-nordisk-ends-collaboration-with-hims--hers-for-discounted-weight-loss-meds-123122046); [AP via WTOP](https://wtop.com/national/2026/02/hims-hers-drops-plan-for-knockoff-of-novo-nordisks-new-wegovy-weight-loss-pill/) |
| **Coverage cliff** | Cigna dropped GLP-1 weight coverage for its own staff (1 July 2026), as did UVM Health. Only 72% of covering employers expect to continue in 2027. | [InsuranceNewsNet](https://insurancenewsnet.com/oarticle/cigna-drops-coverage-of-glp-1-obesity-drugs-for-its-own-employees); [WCAX](https://www.wcax.com/2026/07/17/uvm-health-cutting-glp-1-weight-loss-drug-coverage-employees/); [Pharm. Commerce](https://www.pharmaceuticalcommerce.com/view/why-some-employers-are-scaling-back-glp1-coverage-in-2027) |
| **Cheaper option** | Foundayo launched in April 2026 from $149/month (most patients expected to pay about $349). | [Fierce Healthcare](https://www.fiercehealthcare.com/telehealth/eli-lillys-launches-oral-glp-1-drug-across-us-through-lilly-direct-telehealth-providers) |
| **Bad billing or support** | Hims reviewers describe unwanted resubscriptions and an app that wouldn't let them message the provider. Noom reviews centre on cancellation and Noom Med upsells. | [Trustpilot](https://www.trustpilot.com/review/hims.com?page=2); [unstar.app, vendor](https://unstar.app/blog/noom-cost-charged-after-cancelling-refund-reviews-2026) |
| **Provider failure** | "thank you Pomegranate and Hallandale for the quick delivery," after OrderlyMeds failed. This is Pomegranate's only mention in 2,300 posts. | [1tzqxjx](https://redd.it/1tzqxjx) |
| **Free alternative** | Noom's GLP-1 Companion went free on 24 June 2026; Hers bundles a free smart scale. | [Noom](https://www.noom.com/in-the-news/noom-launches-free-version-of-its-powerful-glp-1-companion/); [Hims & Hers IR](https://investors.hims.com/news/news-details/2026/Hims--Hers-Introduces-New-Hers-App-with-First-of-Its-Kind-Doctor-Led-AI-Native-Care-Experience/default.aspx) |

### Call

**Existing patients** don't "switch apps". They hand over the moments their old app gets wrong, and Pomegranate controls six of them: start of care, each dose step, a new fill or strength, each charge, the first side-effect week, and the plateau and maintenance. At each one, show the truth in one line: "Your dose went up today. Your new vial is 10 mg/mL, so you still draw to 50 units." Never name the competitor. A tracker built on typed-in doses can't say that sentence, and the patient will notice.

**New patients** arrive after a trigger has already happened: a coverage cliff, a failing provider or a cheaper drug. For them, "Bring your history" is the welcome mat. The client research calls the coverage-loss import the "most natural acquisition channel," and the 2026 coverage news makes it urgent.

---

## 3. Lowering the switching cost to near zero

### What can realistically be imported

| Source | What you get | How | Confidence and caveats |
|---|---|---|---|
| **Pomegranate's own records** | Prescriptions, every fill (strength, pharmacy, lot, use-by), messages, visits, labs | Portal single sign-on | **High.** Ground truth; dose history since joining needs no typing. |
| **Apple Health (HealthKit)** | Weight, body composition, waist, protein, workouts, heart and sleep data. From iOS 26, **medications and dose events**, authorised per medication ([WWDC25](https://developer.apple.com/videos/play/wwdc2025/321/)). Labs via Health Records (FHIR) ([Medblocks](https://medblocks.com/blog/how-apple-health-pulls-your-medical-records-the-fhir-stack-explained)) | Read permissions, back-filled once | **High** for weights. Dose events exist only if logged in Health. Third-party *write* is unclear ([Apple forum](https://developer.apple.com/forums/thread/803954)), so treat it as read-only. |
| **Health Connect** | Weight, body composition, nutrition, exercise, sleep, heart data; FHIR medical records including labs (Android 16) | Read permissions | **Medium.** No confirmed medications type ([Android](https://developer.android.com/health-connect)). |
| **Shotsy** | No documented CSV. A **PDF report** with "complete dose history, side effects log, injection sites, and weight trends" ([Shotsy](https://shotsyapp.com/glp-1-side-effects-tracker/), from a search snippet because the site was unreachable). Weight comes from Apple Health. | Weights via Health; PDF parse with review; screenshot OCR as fallback | **Medium-low.** The layout can change, so always review. Costs $9.99/month or $39.99/year ([App Pricing Lab](https://apppricinglab.com/app/apple/6499510249)). |
| **MyFitnessPal** | Premium only: three CSVs (meal nutrition, weight and measurements, exercise). Free users get a PDF ([TakeoutDay](https://takeoutday.org/guides/how-to-export-myfitnesspal-data)). | CSV, or weights via Health | **Medium.** Import weights and measurements, not food diaries. |
| **Generic CSV** | Date, weight, dose (mg or units), site, notes | Column mapping with preview | **High.** Copy Hevy: one import, reversible ([Hevy](https://help.hevyapp.com/hc/en-us/articles/38001424401943-How-to-Import-Strong-App-CSV-Files-and-Export-Your-Data-in-Hevy)). |
| **Progress photos** | Camera-roll photos with EXIF dates | Multi-select, local and encrypted | **High.** Pick a Day 0; never upload by default. |
| **Pen, vial or box photo** | Strength, use-by, lot and pharmacy from the label. Brand cartons carry a DataMatrix with NDC, lot and expiry ([TraceLink, vendor](https://www.tracelink.com/resources/resource-center/pharmacy-packaging-is-changing-will-you-be-ready)). Apple Health has scanned medication labels since iOS 16 ([AppleInsider](https://appleinsider.com/articles/22/06/22/how-ios-16-helps-you-track-manage-and-monitor-your-medication)). | On-device text and barcode recognition | **Medium.** Use it to *check* a vial against the Rx or capture a prior prescription. **Never infer a dose from a photo alone.** DataMatrix on compounded vials is unconfirmed. |
| **Outside labs** | PDF or photo, or Health Records | Upload, then clinician verification | **Medium.** Shows "Not yet reviewed by Dr. Shah" until verified. |

### The "Bring your history" flow

This is an onboarding step after "Here's your plan", and it is also available later under You → Your data.

1. **"Bring what you already have. Optional, about two minutes."** Tiles: Apple Health · Shotsy report · A spreadsheet · Photos · A previous prescription. Each shows what it brings: "weights since March," "doses and side effects."
2. **Review, with provenance on every row.** Each row is labelled *From your prescription* (shown with a seal), *You logged*, or *Imported from Shotsy*. Duplicates merge by date. Conflicts are flagged, never resolved silently: "Shotsy says 5 mg on 15 Sep; your prescription says 2.5 mg until 22 Sep. Keep both, and Ana will check."
3. **The payoff screen.** "Your record now starts 3 March, not today." The trend draws across seven months, with dose steps and the prescribing clinician marked on the line, and the seeds fill in.
4. **Undo at any time.** "Remove everything imported from Shotsy" is one button.

### Keeping the old app alongside

**Call:** say so openly: "Keep using Shotsy for as long as you like."

- Write weights *to* Apple Health so the other apps stay current. Shotsy reads weight from Health.
- Offer free CSV export of everything, in the same format the import accepts.
- After 30 days, ask once: "Still logging doses in another app too?" Use the answer as a metric and never as a nudge.

This copies how Hevy treats Strong users. Coexistence lowers risk and builds trust, and the prescription-sourced dose screen does the persuading.

### What the first five minutes must deliver

| Minute | What the patient sees | Why the old app now feels worse |
|---|---|---|
| 0–1 | Sign in with the existing Pomegranate account and Face ID. No new password. | Shotsy and MFP start with forms. |
| 1–2 | **"Here's your plan, Denise":** tirzepatide 5 mg weekly, a 10 mg/mL vial, **draw to 50 units**, next dose Tuesday, refill ships Saturday at the stated price. Nothing is typed. | Typed-in doses can't know the vial. |
| 2–3 | **Your team:** Ana López RN and Dr. Shah, with photos, "usually replies within 1 business day," and any open thread with its honest status. | A PDF is not a person. |
| 3–4 | **Bring your history:** seven months of Apple Health weights, plus dose steps from Pomegranate fills. | The old chart has no "who changed my dose and why." |
| 4–5 | **One next step:** "Your next dose is Tuesday. 50 units." Reminder set. Readability choice and privacy promises already made. | The cue (dose-day morning) now lives here. |

Measure this with time to first value under 60 seconds, the share of plan fields pre-filled (target 100%), and the correction rate ("Something looks different" taps).

---

## 4. The "can't get it elsewhere" moments, ranked

We scored each moment 1–5 on four things:

- **Unique:** can a consumer app copy it?
- **Frequency:** how many patients meet it in the first 90 days?
- **Intensity:** how emotionally charged it is, using discontinuation drivers from the client research
- **Tellable:** can it be said in one sentence to a friend?

| Rank | Moment | The sentence a patient tells a friend | U | F | I | T |
|---|---|---|---|---|---|---|
| 1 | **Closed loop: your log changes your care** | "I said I was nauseous at 9:41. It showed me Ana read it, and by lunch Dr. Shah had sent something to my pharmacy." | 5 | 4 | 5 | 5 |
| 2 | **Dose in syringe units from the prescription, with the new-strength check** | "My new vial was double strength and the app told me to draw 25, not 50." | 5 | 3 | 5 | 5 |
| 3 | **Return after absence** | "I disappeared for three weeks. No guilt trip; it told me whether I could restart at my dose." | 4 | 4 | 4 | 4 |
| 4 | **Visit brief** | "My doctor had already read my week. I didn't have to explain anything." | 4 | 3 | 3 | 4 |
| 5 | **Refill and cost honesty** | "It told me the price before charging me, and when I was stretching doses they offered a plan, not a lecture." | 4 | 3 | 4 | 3 |
| 6 | **Maintenance with a clinician-set taper** | "They actually have a plan for after. I know my range, and they check in if I drift." | 5 | 1 now (high later) | 5 | 4 |
| 7 | **Fill transparency card** | "I can see the pharmacy, lot and use-by date for every vial." | 4 | 3 | 3 | 3 |
| 8 | **Labs with the doctor's note** | "My A1c is back in range, and Dr. Shah wrote what it means." | 3 | 1 | 4 | 4 |

### Call

The prototype already contains moments 1–5, but it shows them as *process*: statuses, chips and cards. Each needs a visible **outcome receipt** in plain words:

- **Moment 1:** a "What changed because you told us" line on the loop's final step, carried into the timeline. For example: "Because you reported nausea: anti-nausea prescription sent to Larkspur, 1:58 pm."
- **Moment 4:** a read receipt on the brief: "Dr. Shah opened your brief at 10:12."
- **Moment 2:** a dedicated dose-day variant when the strength changes.
- **Moment 6:** a demo state now. It is the longest phase, and no competitor serves it.

---

## 5. Identity audit and an ownable system

### 5.1 What is borrowed, and what replaces it

| Element in the prototype | Where it comes from | Verdict | Ownable replacement |
|---|---|---|---|
| Chartreuse #E7FE55 "now" needle and dot (ruler, hold ring, capsule, loop dot) | Veri's yellow needle | **Borrowed**, and the most visible accent | An **oxblood seed outline** marks "now" and fills when done. |
| Tick ruler with fixed needle (weight, waist, workout) | Veri | Borrowed; keypad-first is in progress | Keypad first with one-tap "Same as last time"; the ruler stays an option. |
| Hold ring with 72 ticks and a rotating needle | Veri dial | Borrowed | **Seed fill** (5.7). |
| Dark "aura stages"; palette names Rare Jade, Tranquil Lavender, Floral Magenta | Veri's own swatch labels | **Borrowed, names included** | One light world on ivory with category tints (5.3). "Jewel Dark" (oxblood-black) is a system dark mode, not an input stage. |
| Dot-matrix numerals | Veri | Borrowed (removal in progress) | Serif hero numerals, tabular. |
| Trend line crossing behind a person into a frosted capsule; wavy panel edge | Vessel's "Wellness" card | **Borrowed**; it is the Today hero | An ivory **week band**: one plum line, dose days as seeds on the axis, today as an oxblood seed outline. No figure behind data. |
| Dark pill with a white orb | A common pattern, also in Veri | Generic | An **oxblood pill** with an ivory label for the one primary action. |
| Glowing mood orbs | Veri | Borrowed | Word rows (Rough · Low · Okay · Good · Great) on paper. |
| Geist Light display, Geist Mono uppercase labels | Vercel's typefaces | Generic, and hard to read (§7) | Season Mix plus Google Sans Flex (5.4). |
| Single-line profiles (woman; men's references) | Stock "one line art" genre; licence unconfirmed | **Unownable, legal risk** | Commissioned set (5.5). |
| Misty landscapes with tiny figures (CC BY, no releases) | Generic "wellness fog" | Unownable; fog signals *unclear* | Commissioned photography (5.6). |
| Seed record as a golden-angle spiral (`arilSVG`) | A sunflower spiral | Right idea, wrong fruit | Chambers and seeds (5.2). |

**Already ownable, so keep and elevate these:**

- "Your treatment, with people who answer."
- The honest message status ("Delivered… Not read yet.")
- "Nothing to catch up on"
- "What Dr. Shah reads first"
- The mg / mL / units chips
- "Share it without numbers"
- "No surprise charges. Messages are never charged."
- The plateau explainer

These are behavioural identity, which is the harder kind to copy.

**The colour finding.** Pomegranate's brand colours, pomegranate red #861A26, deep oxblood #660C21, weight-loss #841839 and men's teal #1B414A ([client research](./Pomegranate_progress_tracker_research.md)), appear nowhere in the prototype. The only near-oxblood is the alert colour #7A1527. **Call:** the brand's colour must mean *your record and your next step*, not danger.

### 5.2 The signature motif: seeds and chambers

**The fruit.** A pomegranate holds a few hundred seeds packed into irregular chambers (locules) separated by pale membranes ([ASHS](https://ashs.confex.com/ashs/2016/webprogram/Paper24007.html); [Foods 2023](https://mdpi-res.com/d_attachment/foods/foods-13-00201/article_deploy/foods-13-00201.pdf)). Because they are packed tightly, real seeds are **faceted**, not teardrops.

**Mapping rules (non-negotiable):**

- **One seed = one treatment week.** A week counts if the dose was taken (weekly injection) or most doses were taken (daily pill). The same rule works for oral GLP-1s, TRT and LDN.
- **One chamber = one chapter of care**: Starting 2.5 mg, Step 5 mg, 7.5 mg, Steady range (maintenance), Taper. A chamber's size grows with its weeks.
- **A missed week is a soft outline, never removed and never red.** A **clinician-approved pause** (illness, surgery) is a seed with a small rest dot. It counts as care, not as missing.
- **The fruit only grows.** There are no resets, scores or comparison, and nothing in it can be bought or earned twice.

**Applications (at most one per screen):**

1. **Today.** A small fruit glyph beside "Week 10". On the week band, today's marker is an oxblood seed outline that fills when the dose is recorded.
2. **Dose day.** The hold-to-confirm fills a single seed. On release it settles into its chamber (5.7).
3. **Chapter close.** When the clinician changes the dose step, the chamber's membrane draws closed and the chapter recap opens: "Chapter 2 · 5 mg · 6 weeks." This hands directly to the Wrapped-style recap now in progress.
4. **Return after absence.** The fruit shows the gap as soft outlines: "Your record is safe."
5. **Share card.** Your fruit as an abstract pattern, unique to your history, with no weight, drug or dates. Caption: "10 weeks in."
6. **Maintenance.** Weeks in the steady range get a sage rim, so "12 weeks in range" can be seen and counted.
7. **App icon and lock screen.** A single faceted seed on ivory or oxblood, with nothing medical.

**Cliché check, and how to avoid it.** The pomegranate carries heavy symbolism (fertility, Persephone, abundance), and fruit motifs easily become twee. The specific danger is that **a red droplet beside an injection reads as blood.** The rules:

- Seeds are faceted and translucent, with a highlight, and usually shown packed together. A single seed never sits next to needle imagery.
- No juice, splashes or cartoon fruit.
- No puns ("seeds of change", "ripe for it").
- The motif is never named in feature titles.
- The motif is always a data structure. If a seed doesn't mean a week, it doesn't appear.

On that basis the motif is meaningful rather than gimmicky, and it is the brand's to own.

### 5.3 Colour roles, from the brand palette

| Role | Colour | Means | Never used for |
|---|---|---|---|
| Canvas | Warm ivory #F4EEE6; paper #FFFCF7 | Calm, the default | — |
| **Your record and your next step** | Oxblood #861A26 (primary pill, seeds), deep #660C21 (pressed) | "This is yours" and "do this next" | Alerts or errors |
| Treatment and dose day | Dusty rose #D9A3A0 / #F0DEDA | Dose surfaces and fill cards | Mood |
| Care team and support | Misty mauve #E4D7E1 | Care tab, messages, the return | Clinical status |
| Steady and in range | Rich muted greens: sage #B9CCBD, olive #4E5A36 | Pace band, steady range, labs in range | "Good versus bad" judgement on weight |
| Data ink | Muted plum #5B2E4E | Chart lines, links | Body text on tints (use ink) |
| Text | Ink #1C1A1B; secondary #3D383A | All text | — |
| **Urgent** | A flat signal-red surface (for example #B42318) with an icon, the word "Urgent" first, and square corners | Act now | Brand moments |
| Category tints | Weight #841839, men's #1B414A, longevity #4E5A36 / #D6E3BE | Each treatment line's chamber and header | — |

Chartreuse is retired. Contrast checks (WCAG formula): ivory on oxblood 8.3:1, white on signal red 6.6:1, plum on sage 6.4:1, ink on mauve 12.5:1, and ink on rose 8.0:1. Seen together, the urgent surface is flat, square-cornered and labelled in words, and oxblood is never flat full-bleed, so the two can't be confused even for colour-blind users.

### 5.4 Type pairing and scale

- **Production display:** **Season Mix** by Displaay ([Maxibestof](https://maxibestof.one/typefaces/season-mix)). This is the brand's own serif, but the live site serves a *trial* file (client research), so buy a mobile-app embedding licence.
- **Production UI:** **Google Sans Flex**, now open source under the SIL OFL with weight, width, optical-size and roundness axes ([Fontsource](https://fontsource.org/fonts/google-sans-flex/about); [OMG! Ubuntu](https://www.omgubuntu.co.uk/2025/11/google-sans-flex-font-ubuntu)). This settles the client research's open question about the Google Sans licence. Verify tabular figures before using it in charts.
- **Prototype stand-in:** Newsreader (opsz 72) for Season Mix, and Google Sans Flex itself for UI. Both are free on Google Fonts.

| Style | Standard | Clear text |
|---|---|---|
| Hero numeral (units, % lost) | Serif 56/60, 400, tabular | Serif 64/68, 500 |
| Screen title | Serif 32/38, 400 | Sans 32/38, 600 |
| Section title | Sans 22/28, 500 | Sans 24/30, 600 |
| Body | Sans 17/24, 400 | Sans 20/28, 450–500 |
| Secondary | Sans 15/21, 400, ink-2 | Sans 18/25, 500, ink |
| Label (replaces mono caps) | Sans 13/16, 600, sentence case | Sans 16/20, 600 |
| Minimum anywhere | 13 px | 16 px |

Serif italics are allowed only at 17 px and above, for one human sentence per screen, never for numbers or instructions. Monospace is gone.

### 5.5 Illustration direction and the brief

**Ownable rule:** *one continuous line that ends in a seed.* Every figure is drawn in a single unbroken stroke, and the pen lifts at a small faceted oxblood seed placed somewhere meaningful: in a hand, on a windowsill, at the end of a walk path. That is a signature no stock vector has.

**Brief for an illustrator:**

- **Cast, 12 figures:**
  - Denise, 52, mid-size, in 4 crops
  - Joe, 47, broad-shouldered, larger body, in 4 crops
  - a woman in her 60s
  - a man in his late 30s
  - a South Asian woman in her 40s
  - a Black man in his 50s
  - Bodies at real sizes, not thin "after" bodies.
- **Scenes:** ordinary moments.
  - holding a mug at a kitchen table on dose-day morning
  - carrying groceries up stairs
  - walking a dog
  - tying shoes on a step
  - reading a phone on a sofa
  - laughing with a friend
- **Never show:** scales, tape measures, before and after, needles in skin, gym glamour, or a body offered as the achievement. Keep the existing rule that milestones show the face only.
- **Objects, 6 studies:** a cut pomegranate (the brand mark), a glass of water, shoes by the door, a fridge shelf, a calendar, a phone face-down.
- **Technical:**
  - SVG, one stroke per path, delivered in drawing order (for draw-on animation)
  - 1.75 pt stroke at 390 pt width
  - single colour, recoloured in code (plum-ink on ivory, ivory on oxblood)
  - Every drawing must still read at 64 px.
- **Licence:** full buyout, perpetual, all media, with the right to modify.

### 5.6 Photography direction

Commissioned and model-released.

- **People:** real people aged 35–65 at eye level in warm interior daylight, with natural skin and everyday clothes.
- **Hands and still lifes:** a pomegranate on linen, water, shoes, a kitchen counter.
- **Grade:** to ivory, rose and sage.
- **Placement:** content pages only (Week one, Month two, hard weeks), never behind data.
- **Avoid:** fog, silhouettes, tiny figures in vast landscapes, gyms, food-as-temptation.

### 5.7 Signature interactions and motion moments (not from Veri or Vessel)

1. **Seed settles (dose recorded).** Hold, and the seed fills from its facets inward over 1.15 s (the deliberate-confirmation time stays). On completion it lifts 6 px and travels along a short arc into its chamber, where neighbouring seeds shift by 1–2 px to make room. Uses a soft spring of about 600 ms. The haptic is "Settle" (5.10). Under Reduce Motion the seed appears filled in place.
2. **Chamber closes (chapter end).** The pale membrane draws around the finished chamber in about 900 ms, the chapter label sets in serif, and the recap opens. It is used only on a real clinical change, so it keeps its weight.
3. **Brief folds (weekly check-in or visit brief).** The week's three or four answers stack and fold into one card. The card moves into the care thread and shows the honest status ("Sent 9:41 · Delivered 9:42"). This makes "never re-explain" visible.

The travelling loop dot stays, but it becomes plum ink on a membrane-like line instead of chartreuse.

### 5.8 Rituals

- **Dose day.** The reminder carries the units. Then:
  1. Vial check: the label matches the prescription; otherwise a "Strength changed" variant appears.
  2. The syringe shown at true scale.
  3. Choose the site.
  4. Hold, and the seed settles.
  5. "Next dose Tue 27 Oct."
- **Weekly check-in**, on a day the patient chooses, in 30–45 seconds:
  - weight (optional)
  - food noise (section 6)
  - one feeling word
  - protein days
  - "anything for Ana?"
  - The brief folds and is sent.
- **Chapter close.** Triggered by the clinician, never by the app.
- **The return.** No backlog, one next step, restart rules from the clinician.

### 5.9 Voice, tone and naming

**Principles, with example lines:**

| Principle | Write | Not |
|---|---|---|
| Number first, then meaning | "Down 0.6 lb since Tuesday. Your 7-day average is what counts." | "Great progress!" |
| Name the person | "Ana read your message at 10:14." | "Your request is being processed." |
| Honest about time | "It's Friday evening, so expect a reply Monday morning." | "We'll be in touch soon." |
| Credit the patient | "You did the work; the medicine is a tool." | "Ozempic magic!" |
| Neutral about lapses | "Welcome back. Nothing to catch up on." | "You missed 2 doses 😢" |
| Say the plan, not a judgement | "If your average stays above 168.5 lb for two weeks, Ana will check in. That's the plan, not a failure." | "Warning: weight regain" |
| No moralising, no cheer | No "cheat", "guilt-free", exclamation marks, emoji or confetti | — |
| Short and plain | One idea per sentence, grade 6–8 | — |

**Feature names:** plain words only.

- Today
- Your record
- Care
- Dose day
- Weekly check-in
- What Dr. Shah reads first
- Fill details
- What you'll pay
- Steady range
- Lab results
- How your week usually goes
- Our promises
- Clear text
- Bring your history

**Banned words:** Journey, Insights, Score, Coach, Buddy, Streak, Hub, Wellness, and any "AI" branding.

### 5.10 Sound and haptics for the native app

**Principles:**

- Haptics confirm; they never nag.
- Sound is off by default and respects the silent switch.
- Every haptic has a visual twin.
- Urgent states use no custom haptic or sound beyond the system's.

| Name | When | iOS (Core Haptics / UIFeedbackGenerator) | Android (VibrationEffect.Composition) |
|---|---|---|---|
| Tock | Choosing a chip or row | Light impact | PRIMITIVE_TICK |
| Settle | Dose recorded | One soft transient plus a 120 ms decaying continuous tail | CLICK then LOW_TICK |
| Close | Chapter closes | Three soft transients 90 ms apart, rising | QUICK_RISE |
| Check | "Is 180.2 lb right?" | A single light tap, not an error buzz | TICK |

The optional sound is a low, warm, felt-piano "pip" of about 300 ms, used only for Settle and Close. In React Native, `expo-haptics` covers Tock and Check. Settle and Close need a small native module (AHAP patterns on iOS, compositions on Android API 30+; see [Core Haptics](https://developer.apple.com/documentation/corehaptics) and [VibrationEffect.Composition](https://developer.android.com/reference/android/os/VibrationEffect.Composition)).

---

## 6. Gaps against the client's research: designs ready for the prototype

| Gap | Design in the light, calm system | In the concept? |
|---|---|---|
| **Maintenance ("Steady range")** | A sage band on the week chart, clinician-set (example: target ±2%). Big serif "12 weeks in your steady range," with sage-rimmed seeds. **Drifting** (+2–3%, mauve outline): "Ana will check in." **Review** (≥ +3% for two weeks, plum outline, never red): "Dr. Shah will review your plan." A taper card ("Step 2 of 4 · 5 mg every 10 days · set by Dr. Shah") with food noise under each step. Modelled on STOP Regain's zones (within 2 lb, 3–4 lb caution, 5 lb or more act) ([MDedge](https://www.mdedge.com/content/weighing-active-intervention-keep-pounds)). Values need clinical sign-off. | **Yes:** a "Month 9" demo state |
| **Food-noise score** | The validated **Food Noise Questionnaire**: 5 items, 0–4 each, total 0–20 ([ConscienHealth](https://conscienhealth.org/2025/01/yes-food-noise-is-real-and-measurable/)). In a 2026 cohort it fell 4.05 points on GLP-1s versus 1.15 points with behaviour alone ([Pennington](https://www.pbrc.edu/news/media/2026/food-noise-eco.aspx)). Ask weekly as five one-tap rows; show a plum line under the dose steps ("Quieter since 5 mg"). Confirm permission from the authors. | **Yes**, in the weekly check-in |
| **Muscle and protein** | Weekly, not a daily verdict: "Protein days: 4 of 7," "Strength sessions: 2," optional lean-mass estimate via Health. Clinician-set target; low intake routes to Ana, not to a red number. 36% rate their muscle-loss risk moderate or higher ([Veru via Fierce Pharma](https://www.fiercepharma.com/marketing/veru-survey-highlights-muscle-loss-concerns-among-glp-1-users-lean-mass-preserving-med)). | **Should** |
| **Fill transparency card** | A rose card per shipment: pharmacy and licence state, 503A/B, strength, volume, lot, use-by, arrival photo, and **"Looks different?"** (cloudy, colour, leak, warm cold pack). That option stops the dose, messages the nurse and is linked to the lot for pharmacy QA. A banner appears when the strength changes. | **Yes:** extend Prescription |
| **Refill and cost ("What you'll pay")** | Next charge and date, what is included, and the maintenance price up front. "Changes only with notice" (a commitment for the client to confirm). Pause or cancel in two taps. **"Running low or stretching doses? Talk to us about a plan."** Refills never gated on app use. | **Yes** |
| **Labs timeline** | Draws by date: plain-word markers, a sage "in your range" pill, and the clinician's note. A flagged result reads "Dr. Shah will call you," never just a red value. Upcoming orders; Health Records import. Joe's TRT markers use the same component. | **Should** |
| **Dose-response curve** | "How your week usually goes": a rose area behind the week strip, estimated from *your prescribed schedule* and published half-lives, with symptoms as dots. Labelled "Estimate to help you understand your week. Not for changing doses." Personal patterns only after 4 or more weeks. Shotsy paywalls a similar chart ([GLP3 Planner, competitor](https://glp3planner.com/resources/shotsy-alternatives)). | **Should**, as an explainer |
| **Category awareness** | Each treatment line has its own chamber tint and appears on Today in date order ("Tonight: LDN 1.5 mg · Tuesday: tirzepatide"). TRT: twice-weekly schedule, labs first. LDN: daily, **no streaks**. Hair and skin: monthly same-angle photos. Naltrexone can use a neutral label and never appears in sharing. | **Should**, in Joe's persona |

---

## 7. Legibility for 35–60, and the "Clear text" mode

### Evidence

- **Eyes.** Most people need reading glasses by 45 ([InformedHealth](https://www.informedhealth.org/presbyopia.html)), and the core patients are 35–60.
- **Size.** Older adults prefer larger, sans-serif text of at least 14 pt on mobile. Age-friendly design centres on larger text and targets and simpler navigation ([Frontiers 2022](https://www.frontiersin.org/articles/10.3389/fpsyg.2022.931646/full); [2025 review](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12350549/)).
- **Weight.** Older readers are more sensitive to font differences, and light weights fail at small sizes ([Beier & Oderkerk, Visible Language](https://journals.uc.edu/index.php/vl/article/view/4654)). The lightest weights degrade most when rendering is poor ([Dobres et al.](https://rosap.ntl.bts.gov/view/dot/43887/dot_43887_DS1.pdf)).
- **Capitals.** All-caps works for single words read at a glance but hurts sentences ([NN/g](https://www.nngroup.com/articles/glanceable-fonts/)).
- **Targets.** 44×44 pt on iOS and 48×48 dp on Android, spaced 8 dp apart ([Android](https://support.google.com/accessibility/android/answer/7101858)).
- **System text size.** One developer's stats show 11.5% of users choose larger text ([David Smith](https://www.david-smith.org/blog/2023/01/24/design-notes-19/)). Another app saw 27% use a non-default size ([Nutrient](https://www.nutrient.io/blog/improving-dynamic-type-support/)). No platform-wide figure exists.

### Audit of the prototype

- **Uppercase monospace labels** run 9.5–12 px and carry meaning: "NEEDS ATTENTION TODAY", "DONE FOR THIS WEEK", "20 OCT · WEEK 10".
- **Serif italics** appear at 12.5 px, and body text is often 13–14.5 px.
- **Display type** is Geist 300.
- **Muted text on sage** (#625A5E on #B9CCBD) measures **3.96:1**, which fails AA for small text. Verify it against the real hero gradient.
- **Chartreuse on ivory** is 1.03:1, so it relies entirely on its dark ring.
- **Inline text links** ("Missed or late?", "Needle tips") are small targets.

### Rules for the prototype

1. Body at least 17 px. Secondary at least 15 px. Nothing below 13 px in Standard or 16 px in Clear.
2. No weight below 400 under 28 px. Display at 400–500.
3. Sentence-case sans labels instead of uppercase monospace. Never put essential information in a label alone.
4. Serif italics only at 17 px and above, and never for numbers, instructions or status.
5. Text on tints and glass must reach 4.5:1 against the *lightest* pixel behind it. Use ink, not muted, on sage, rose and mauve, and solid surfaces behind text on glass. Chart lines and markers need 3:1.
6. Targets at least 44 pt, or 48 dp on Android. Primary actions 56 px tall. Text links become full-width rows.
7. Never rely on colour alone: icon plus word for status, patterns in charts.
8. Plain words: "Use by", not "BUD"; "Dose step", not "titration"; "50 units", never "50u".

### The "Clear text" mode (must-have for the concept)

**What it changes.** It applies the Clear column of the type scale (5.4) and makes these other changes:

| Change | Detail |
|---|---|
| Size | Body 20 px, secondary 18 px, labels 16 px |
| Weight | 450–600 instead of light weights |
| Labels | Sentence case, no monospace |
| Italics | None, and no small serif |
| Text colour | Ink only, 7:1 target for body |
| Surfaces | Solid behind all text; no glass or blur |
| Targets | 52–60 px rows and buttons |
| Motion | Reduced motion offered as a linked switch, on if the system says so |
| Charts | A "Show as list" alternative is always present |

**Where it lives.** Onboarding asks one question, framed as a preference: **"How do you like to read?"** It shows two equal, live previews of the same Today card, *Standard* and *Clear*, with "Some people prefer bigger, bolder text. Switch any time." You → Display has *Standard · Clear* at the top. The demo menu lets reviewers flip any screen.

**System settings.**

- **Always follow the system text size** (Dynamic Type, Android font scale) in both modes. Clear changes weight, case, surfaces and targets, *not* the user's chosen size.
- **Pre-select Clear** in onboarding if Bold Text is on or the text size is above default.
- Honour Increase Contrast, Reduce Transparency, Reduce Motion and Differentiate Without Color individually, even in Standard.
- In React Native, keep `allowFontScaling` on, cap only hero numerals (`maxFontSizeMultiplier` about 1.4), and read `AccessibilityInfo`.

**Reflow at the largest sizes, keeping one primary action:**

- Single column: tiles stack; chips and segmented controls become radio rows.
- The **primary action sits directly under the headline**, full width, with its label wrapping to two lines. Sticky footers un-stick above 20% of the viewport. Secondary actions are listed *below* it, never beside it.
- Dose, units, names and times **wrap; they never truncate**. Tab labels stay visible, with the iOS large-content viewer on long-press.

**First-class, not an afterthought:** call it a style, not a fix. Design and QA every screen in both modes. Use Clear in marketing screenshots and in Joe's persona. Make the share card and recap respect it. Apple's 2026 design awards rewarded this depth of Dynamic Type support (client research).

---

## 8. Men: what changes, without making the app gendered

### Evidence

- **Hiding treatment.** In a 2026 UK pharmacy survey, just over half of men hid their weight-loss treatment, against nearly 70% of women. 28% of men felt judged, against nearly 40% of women ([EMJ](https://www.emjreviews.com/general-healthcare/news/two-thirds-of-weight-loss-drug-users-treat-in-secret/)).
- **Willingness to share.** In the US, 69% are unlikely to tell others they take a GLP-1. Men are slightly more likely to share (34% versus 29% of women) ([Virta Vitals 2026](https://www.virtahealth.com/press/2026-virta-vitals-the-rise-of-the-glp-1-era)).
- **Social penalty.** A 2026 Rice study (n = 607) found GLP-1 users were rated less honest, warm and intelligent than people who lost weight otherwise, or who didn't lose weight at all ([Rice](https://news.rice.edu/news/2026/glp-1-paradox-rice-study-finds-weight-loss-drugs-may-carry-unexpected-stigma)).
- **Masculinity framing.** A physician describes online masculinity content casting medication as weakness, set against "discipline" ([MDLinx](https://www.mdlinx.com/article/glp-1-stigma-is-different-in-men-here-s-how-to-cut-through-it/4v9Pf0v22Wu9NNjTndrVSr), from a search snippet).
- **App use.** In one mHealth weight-loss trial, women opened the app more. Men shared results and used live tracking more ([JMIR Formative](https://formative.jmir.org/2022/10/e38480)).
- **TRT secrecy.** "No one except my wife knows I'm on TRT" ([1sj2qpm](https://redd.it/1sj2qpm)).

### Call

**Don't gender the app. Gender-neutral choices serve men without labelling them.**

- **Progress priorities are chosen, not assigned.** In onboarding, ask "What matters most to you?" with options for energy, labs, strength, how clothes fit and weight. The answer reorders the Progress page. Joe picks labs and strength; Denise picks how clothes fit and weight.
- **Framing.** Lead with function: waist, strength sessions, blood pressure, A1c, haematocrit, and "muscle kept." Weight comes second. Copy credits work and calls the medicine a tool, which answers the "weakness" narrative without arguing with it.
- **Tone.** Use the same voice with fewer feelings prompts by default. The mood check stays one tap away rather than the first thing shown. Numbers first, no pep.
- **Imagery.** Joe and men in their 40s–60s in ordinary scenes: carrying, walking, cooking. No gym bros and no shirtless "after."
- **Privacy for everyone, which men will use most.**
  - a neutral app icon option (a plain seed on ivory, with no name)
  - lock-screen text that is already free of medicine
  - discreet notification wording
  - the share card already hides numbers and drugs
  - a "partner can see" setting only for behaviours, never for weight or medication

---

## 9. Trust: what this audience rewards and punishes

### Evidence

- **Rewarded:**
  - reachability: "They answer the phone every time I call" ([1ujrabl](https://redd.it/1ujrabl))
  - Shotsy's "no data harvesting"
  - Hevy's free history
  - Strava's public apology for a confusing price rollout (client research)
  - Relational bonds are the strongest staying force ([Burnham et al.](https://journals.sagepub.com/doi/10.1177/0092070302250897)).
- **Punished:**
  - **Upsells to people already paying:** the WHOOP member who wanted "to turn off AI & ALL ads", and complaints about Noom Med upsells.
  - **AI that invents things:** Oura's Advisor "admitted it made it up" ([1rnr2td](https://redd.it/1rnr2td)). Only 29% of adults trust AI chatbots for health information ([KFF, Aug 2024](https://www.kff.org/health-information-trust/poll-most-who-use-artificial-intelligence-doubt-ai-chatbots-provide-accurate-health-information/)).
  - **Data sales and leakage:** Cerebral's $7M settlement, the Flo/Meta verdict, and 23andMe's deletion wave.
  - **Dark-pattern billing:** Noom's $62M settlement.
  - **Retroactive paywalls:** Garmin and WHOOP.
  - **Care conditioned on app use:** coverage revoked by an insurer's app mandate ([1uygcr5](https://redd.it/1uygcr5)).

### Call: publish "Our promises"

Put this on one screen, linked from onboarding's privacy step, from You, and from the footer of Care. Each promise has a "How you can check" line.

1. **A person answers.** Messages are answered within 1 business day, and you always see when yours was delivered and read. *Check: the status on every message.*
2. **Your care never depends on this app.** Refills, visits and prescriptions never wait for logs.
3. **No ads, no selling or sharing your data for marketing, no ad trackers in the app.**
4. **Your history is yours.** Export everything, free, at any time. Delete on request.
5. **Nothing about your health on your lock screen.**
6. **No surprise charges.** You see the price before you're charged, prices change only with notice, and you can cancel in the app.
7. **Only your clinician changes your dose, with you.** Anything automated is labelled, comes only from your own data, and never advises a dose.
8. **If something is wrong, we tell you first:** a late reply, a recalled lot, or a price change.

Once real operations data exists, add a monthly "Last month, median reply: 5 h 12 m" line. Avoid the phrase "bill of rights" until counsel reviews it, because it implies legal guarantees.

---

## 10. Measurable hypotheses and how to test with 5–8 people

### Hypotheses for the concept

| # | Hypothesis | Concept measure (n = 8) | Beta measure |
|---|---|---|---|
| H1 | **Return after absence:** a no-backlog return makes a forward action more likely than a "missed doses" screen | Within-subject A/B (current return screen versus a "You missed 2 doses, get back on track" control, counterbalanced). Measures: chosen action, guilt on a 1–5 scale, time to action. Target: at least 7 of 8 choose a forward action, guilt at least 1 point lower | Share of patients away 7 or more days who log a dose within 7 days of return; time to next dose |
| H2 | **Switching intent:** a 5-minute pre-filled plan plus "Bring your history" moves the dose habit | 0–10: "How likely are you to log your next dose here instead of [current app]?" Plus the behavioural choice: do they set the Pomegranate reminder and *say* they would turn the other one off? | Share of doses logged in Pomegranate by week 4. The "Still using another app?" answer. The Sean Ellis "very disappointed" share, aiming for at least 40% with n ≥ 40 ([Learning Loop](https://learningloop.io/plays/product-market-fit-survey)) |
| H3 | **Month-two persistence:** the plateau explainer and visit brief reduce stop or pause intent | In the plateau scenario: "What would you do next?" Target: at least 7 of 8 choose "keep going" or "message Ana" over pause, stop or buy elsewhere | Dose-log persistence at day 60 and refill persistence at day 90, against a matched pre-app cohort, with the plateau card randomised |
| H4 | **Loop outcome receipts raise trust** | Agreement with "I know what happens next" after the nausea loop, with and without the "What changed" line | Reply-time SLA met; repeat reporting |
| H5 | **Clear text helps without stigma** | Dose task errors and time in both modes; preference; "Would you leave it on?" | Uptake of Clear text; uptake by system text size |
| H6 | **The seed motif is understood and not misread** | "What does a pale seed mean?" with no explanation. Target: at least 6 of 8 say "a missed week" and 0 say blood, failure or loss | — |

### A 5–8 person test before the native build

**Recruit 8 current patients:** 5 women aged 35–60 (at least 2 aged 55+), and 3 men (1 on TRT plus a GLP-1). Mix their current tools: 2 Shotsy, 2 Apple Health or MFP, 1 Oura or WHOOP, 1 with no tracker, 1 who came from Hims, and 1 who moved from insurance to cash pay. Include at least 2 who wear reading glasses. Test **on their own phones at their own text size.**

**Session plan, 60 minutes:**

1. **10 minutes:** "Show me your last dose log" in their current app.
2. **10 minutes:** first run, with their *own* plan and real history pre-loaded from a screenshot (Wizard of Oz).
3. **25 minutes of tasks:** dose day with a new vial strength; report nausea and follow the loop; the return after 10 days (the A/B); "What will you pay next month?"; maintenance drift; turn on Clear text.
4. **15 minutes:** switching-intent questions; "Which moment would you tell a friend about?"; rank the promises; explain the seed record; Sean Ellis question (intent version).

**Follow-up:** a 10–14-day diary pilot with 5 of them, with a real nurse answering in a test thread. Record which app they actually logged doses in.

**How to read it:** five users surface most usability problems ([NN/g](https://www.nngroup.com/articles/why-you-only-need-to-test-with-5-users/)), but preference and intent from eight people are directional. Report quotes and counts, not percentages.

---

## PROTOTYPE BACKLOG

The list is prioritised. **Must** marks a must-have for the concept. Effort: S under a day, M one to three days, L more than three days or external.

| # | What to build | Screen | Why it moves switching or retention | Evidence | Effort |
|---|---|---|---|---|---|
| 1 | **Bring your history.** Source tiles (Apple Health, Shotsy report, CSV, Photos, previous Rx), a review screen with provenance labels, a conflict flag, "Your record now starts 3 March", and undo | Onboarding (after the plan) and You → Your data | Cuts procedural cost to near zero, and makes the record richer than the old app's in five minutes | Shotsy PDF-only export; MFP Premium CSV; HealthKit iOS 26 reads; Hevy's reversible import (§3) | M · **Must** |
| 2 | **Dose day from the prescription, with the new-strength check.** A "Strength changed" variant (same 2.5 mg dose, but the vial is now 10 mg/mL instead of 5 mg/mL: draw to 25 units, not 50), a vial-label photo matched against the Rx, and the syringe at true scale | Today (dose day) and Dose stage | The #2 tell-a-friend moment, and the trigger consumer trackers can't match | Concentration-change and 10× error posts; prescription ground truth (client research) | M · **Must** |
| 3 | **"What changed because you told us" receipts.** A last loop step stating the outcome; a timeline entry linking report to prescription change; "Dr. Shah opened your brief at 10:12" | Care thread, Progress timeline, Visit brief | Turns the closed loop (#1 moment) into a sentence people repeat | Human feedback is the only add-on with an effect (Antoun 2022); "never re-explain" | S · **Must** |
| 4 | **Clear text mode.** An onboarding preview choice, You → Display, follows system size, the full Clear spec, reflow rules, demo-menu flip | Global, Onboarding, You | Age 35–60 legibility; treated as a first-class mode it raises trust and comprehension | Presbyopia by 45; age-friendly design reviews; prototype at 9.5–12 px mono (§7) | M · **Must** |
| 5 | **Seed-and-chamber record with its motion.** Seed = week, chamber = chapter, gap outlines, pause dots; "Seed settles" on dose; "Chamber closes" at a step change; used on Today, return, the recap and the share card | Today, Dose stage, Progress, Return, Recap, Share | The ownable signature; a quiet record that only grows; feeds the chapter recap in progress | Broken streaks demotivate (Silverman & Barasch); comeback rewards (Milkman 2021); pomegranate anatomy (§5.2) | M · **Must** |
| 6 | **Retire the borrowed signatures.** Chartreuse marker becomes an oxblood seed outline; hold-tick ring becomes seed fill; capsule and figure hero becomes the ivory week band; aura stages and Veri palette names become light category tints; mood orbs become word rows; the wavy edge and orb buttons go | Today, Dose, Mood, Onboarding, Progress | You can't be worth switching to if you look like someone else's case study | Side-by-side with the Ron Design Lab references (§5.1) | M · **Must** |
| 7 | **Brand tokens: colour roles and type.** Oxblood as record and primary action, a separate flat signal-red for urgent, category tints; Newsreader plus Google Sans Flex stand-ins for Season Mix plus Google Sans Flex; sentence-case labels instead of Geist Mono | Global | Makes Pomegranate recognisable and fixes "brand colour = danger" | Brand palette (client research); Google Sans Flex OFL; Season Mix trial-licence issue | M · **Must** |
| 8 | **Weekly check-in ritual.** Patient-chosen day; weight optional, FNQ 5 items, one feeling word, protein days, "anything for Ana?"; the brief folds into the thread with honest status | Today (on check-in day) and Care | Creates the weekly cue Pomegranate owns, and feeds titration and maintenance decisions | FNQ validation and 2026 GLP-1 data; self-weighing works inside accountability (Madigan 2015) | M · **Must** |
| 9 | **Maintenance "Steady range" demo state.** Band, weeks in range, Drifting and Review bands with named human actions, a clinician-set taper card with food noise under each step | Progress, plus a demo menu entry | Serves the longest phase nobody else serves; answers the 56% who fear regain | STOP Regain zones; Healthline 2026; Reddit tapers ([1wpnb34](https://redd.it/1wpnb34)) | M · **Must** |
| 10 | **Fill details and What you'll pay.** A card per shipment (pharmacy, 503A/B, lot, use-by, photo, "Looks different?" which stops the dose) plus a cost card (next charge, maintenance price, notice, pause or cancel, "stretching doses? talk to us") | Care → Prescription, Today on arrival | Trust for compounded medicine and cash-pay certainty, both reasons to stay | Cloudy-vial and COA posts; 68% cite cost; ROSCA; Hims and Noom billing complaints | M · **Must** |
| 11 | **Our promises.** Eight promises, each with "How you can check" | You, Onboarding privacy step, Care footer | Publicly matches Shotsy's "no harvesting" and exceeds it; counters upsell and AI fears | WHOOP, Oura, 23andMe, Noom and Cerebral cases; KFF 29% (§9) | S · **Must** |
| 12 | **Commissioned illustration set.** Ship the brief now; use clearly marked placeholders until the art lands; one line ending in a seed; Denise, Joe and four more ages and bodies | Welcome, Return, Milestone, empty states | Replaces stock with an ownable, licensable signature | Licence unconfirmed (design notes §8) | L · Should (brief is a Must) |
| 13 | **Photography swap.** Commissioned, released, everyday, warm interiors, no fog; content pages only | Week one, Month two, hard-week pages | Removes generic and unreleased imagery; signals clarity | CC BY photos lack model releases | M · Should |
| 14 | **"What matters most to you" priorities and a neutral app icon,** shown in Joe's persona (labs and strength first, TRT twice weekly, labs-first Progress) | Onboarding, You, Progress, Today | Serves men without gendering; privacy for everyone | EMJ, Virta and Rice 2026; i-gendo; TRT secrecy (§8) | M · Should |
| 15 | **Labs timeline** with clinician notes, "in your range" pills, upcoming orders and a Health Records import | Progress → Labs | Lab wins are headline wins; unexplained results drive churn | [1o91taw](https://redd.it/1o91taw), [1sbyysn](https://redd.it/1sbyysn); HealthKit clinical records | M · Should |
| 16 | **"How your week usually goes."** An estimated level curve from the prescribed schedule, with symptoms and food noise; labelled as an estimate | Progress → Dose | Explains nausea timing and builds tolerance; free here, paid in Shotsy | Shotsy paywalls its level chart; GI events raise discontinuation (HR 1.19) | M · Should |
| 17 | **Muscle and protein week.** Protein days, strength sessions, optional lean-mass estimate, low-intake route to Ana | Progress | The second scoreboard; lean-mass fear | Veru survey; client research on protein (0.6 g/kg) | S · Should |
| 18 | **Use both for now.** "Share weights with Apple Health" toggle, free CSV export, a one-time "Still using another app?" question | You → Your data | Coexistence lowers the risk of switching; export is a trust signal | Hevy and Strong precedent; MFP history lock-in backlash | S · Should |
| 19 | **Haptic and sound annotations.** Tock, Settle, Close and Check, noted on screens for the native build; demo via the Vibration API where supported | Dose, Check-in, Recap, Check-number sheet | Gives the native app a recognisable feel without nagging | Restraint as premium (client research); platform haptic APIs | S · Could |

**Concept must-haves (11):** items 1–11. Items 4 (Clear text), 5–7 (the visual identity) and 1–3 (switching) carry the pitch. Items 8–11 prove the service promises behind it.
