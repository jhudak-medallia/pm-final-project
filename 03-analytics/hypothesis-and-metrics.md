# Hypothesis & Success Metrics

> **Module 3 · ★ Deliverable 3.** Repo file `03-analytics/hypothesis-and-metrics.md` — part of your submission.
> It feeds the **Problem, Value & Hypothesis** slide of your Module 6 final deck.

## Finalized product hypothesis

> **We believe** that cutting "Mark Delivered" to one tap from the stop screen and putting "Start Route" on the home screen **for frontline delivery drivers running 40+ stops a day** will raise the share of deliveries confirmed in-app from [baseline]% to [target]% within 8 weeks, **because** drivers currently fall back on texting dispatch and paper manifests rather than navigate 3 screens at each doorstep. **We'll know we're right when** in-app confirmations and time to deliver both improve without route optimizer or dispatch adoption dropping, which should lead to better NPS and fewer at-risk renewals.

## Success metrics

| Metric | Type | Target | Why it matters |
|---|---|---|---|
| % of deliveries confirmed in-app (vs. SMS, WhatsApp or call to dispatch) | Primary (leading) | [baseline]% → [baseline + 20 pts]% by week 8 | Directly measures drivers abandoning the workaround |
| Median time and taps from arriving at a stop to Mark Delivered | Leading indicator | ≥40% reduction | Measures the doorstep friction itself |
| First-attempt proof-of-delivery upload success | Leading indicator | [target]% (from ~65% today) | About 35% of uploads currently fail on weak signal |
| Driver CSAT, account NPS, renewal rate | Lagging outcome | Month-over-month improvement for 3 months | Links the driver experience to retention and revenue |
| Daily adoption of route optimizer, live dispatch and compliance checklist | Guardrail | No drop greater than 5% | Protects the core workflows the existing base relies on |
| Revenue and renewal on accounts that use demoted features (e.g. financial reporting) | Guardrail | No drop greater than 5% | Low-adoption features may still matter to high-value accounts |
| Delivery accuracy and failed-delivery rate | Guardrail | No drop greater than 5% | A faster flow must not cause more errors |
| App crash rate on long routes | Guardrail | No increase | Crashes are what push drivers to paper manifests |

---

## Pre-work · Hypothesis check

- **Role (who you are solving for, from M2):** A frontline delivery driver who runs 40+ stops a day and spends their whole shift in the RouteLogic mobile app.
- **Goal (what this user is ultimately trying to achieve):** Get through every stop quickly and with confidence, without fighting the app at each doorstep.
- **Friction / moment of misery (the specific pain blocking their goal):** Feature bloat has buried the actions drivers repeat all day. "Start Route" (about 30 uses a day) sits 2–3 levels deep, and "Mark Delivered" takes 3 taps across 3 screens, often in bad weather with a package in hand. All 7 focus-group drivers said core-action speed matters more than any new feature. Drivers text dispatch instead, and 5 of 7 carry a paper manifest in case the app crashes on long routes.
- **Current workaround (the external tool or manual process they rely on, from M2):** SMS/WhatsApp messages to dispatch, phone calls to dispatch, a printed paper manifest, phone screenshots of the route, and the driver's own memory of local roads and site access.
  1. **Before the shift:** At the depot, while there's signal, screenshot the stop list and keep a paper manifest in the cab as a backup.
  2. **On the road:** Ignore parts of the optimized route and drive around known closures and access problems from memory, repeating the same corrections every day.
  3. **At the doorstep:** Skip the 3-screen "Mark Delivered" flow and text or WhatsApp dispatch to confirm the drop-off or report a failed delivery.
  4. **Proof of delivery:** Retake the photo up to 3 times, because about 35% of uploads fail on weak signal with no confirmation.
  5. **When the app fails:** Switch to paper or screenshots and call dispatch to have the remaining stops read out, which takes about 20 minutes.
- **Problem Hook (M1):** We must eliminate the unnecessary complexity from the RouteLogic platform that is hindering our core user base from obtaining value from the product and driving them towards competitive alternative solutions, putting our market leadership and customer renewals at risk.
- **Value Proposition (M1, revised):** For frontline delivery drivers who spend their whole shift in the RouteLogic app, we will put the actions they repeat all day, Start Route and Mark Delivered, one tap away and make sure deliveries confirm reliably on weak signal. Drivers can then stop relying on texts, calls and paper manifests, and their fleets get a tool their drivers actually use instead of switching to leaner competitors.

## Read your data snapshots

- **Does the low adoption confirm your persona is burdened by tools they don't use?** Yes. Drivers rarely use the ancillary features: financial reporting (3%), predictive ETAs (11%) and shift scheduling (15%). Their core features see much higher use: live dispatch (88%) and route optimizer (72%). Coordinators use shift scheduling more (42%), but it isn't part of the driver's moment of misery. Low adoption shows these features are unused. It doesn't by itself prove they slow down core actions; the workflow data below is the stronger evidence for that.
- **Does the workflow data match the manual process or hack you documented in M2?** Yes. Completion times for core daily workflows are well above benchmark *[insert actual time vs. benchmark]*. Together with about 35% of proof-of-delivery uploads failing on weak signal, this explains why drivers confirm deliveries by text or WhatsApp and keep paper manifests as a backup.
- **Which CSAT cell maps most directly to your persona's friction, and how does the NPS trend justify the urgency?** NPS has declined steadily for two years, in line with rising churn. CSAT is weak to critically low on features central to the daily workflow. Together these support the urgency of the Problem Hook: the core experience is wearing down satisfaction, and renewals are at risk.

## Step 3 · Craft your hypothesis

- **Qualitative evidence (from M2):** "Start Route" (about 30 uses a day) sits 2–3 levels deep, and "Mark Delivered" takes 3 taps across 3 screens, often in bad weather with a package in hand. All 7 focus-group drivers said core-action speed matters more than any new feature, and 5 of 7 carry a paper manifest in case the app crashes.
- **Quantitative evidence (from M3):**
  - Core workflow completion times are well above benchmark *[insert actual vs. benchmark]*.
  - About 35% of proof-of-delivery photo uploads fail on weak signal, with no confirmation to the driver.
  - 7 of 7 focus-group drivers rank core-action speed above new features, and 5 of 7 keep a paper manifest as a backup.
- **Persona:** A frontline delivery driver running 40+ stops a day. Their goal is to complete every stop quickly and confidently. Their friction is that buried core actions push them onto SMS, phone calls and paper workarounds.
- **Problem you are solving:** Drivers need 3 taps across 3 screens to mark a delivery and 2–3 levels of navigation to start a route, so they bypass the app by texting dispatch and carrying paper.
- **Strategic outcome (the business link):**
  1. **Behaviour change:** Drivers complete Start Route and Mark Delivered in the app instead of by text, call or paper.
  2. **Operational value:** Dispatch gets real-time, accurate delivery status without manual follow-up calls or re-reading routes after a crash (about 20 minutes per incident). Fleets get reliable proof of delivery, which cuts disputes and failed-delivery costs.
  3. **Customer value:** Fleet operators see higher driver productivity and lower dispatch workload, which is the ROI they renew on.
  4. **Business outcome:** Satisfaction recovers (CSAT and NPS), fewer accounts move to leaner competitors or general-purpose tools, and renewal rates are protected. That defends the market leadership named in the Problem Hook.
- **Primary success metrics (leading indicators):**
  - **% of deliveries confirmed in-app** rather than by SMS, WhatsApp or call to dispatch (main metric).
  - **Median time and taps from arriving at a stop to Mark Delivered.**
  - **First-attempt success rate for proof-of-delivery uploads.**
- **Lagging outcome metrics:** Driver CSAT, account NPS and renewal rate.
- **Guardrail metrics (must not drop):**
  - Daily adoption of route optimizer, live dispatch and compliance checklist.
  - Revenue and renewal on accounts that use the features being demoted, such as financial reporting.
  - Delivery accuracy and failed-delivery rate.
  - App crash rate on long routes.
- **Decision window:** 8 weeks from launch to the first decision, then 3 months of monitoring to confirm the trend holds month over month. *(Thresholds are illustrative; set them from your baseline.)*
  - **Scale:** In-app delivery confirmations rise from [baseline]% to at least [baseline + 20 points]%, and time to Mark Delivered falls by at least 40%, with all guardrails stable.
  - **Pivot:** Time to deliver improves but SMS and calls to dispatch don't fall. That means the friction is somewhere else, most likely connectivity or upload reliability, so the focus should move there.
  - **Kill / roll back:** Any guardrail metric falls by more than 5%.
