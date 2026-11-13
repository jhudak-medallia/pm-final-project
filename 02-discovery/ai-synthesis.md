# AI Synthesis — Product Health & Insights Summary

> **Module 2 · Lab 1.** Repo file `02-discovery/ai-synthesis.md` — part of your submission.
> Do the lab in the **Module 2 · Exercise 1 Guide** (linked from the Module 2 deck), then click **⬇ Download .md** — it saves as this exact file. Commit it here.
> It feeds the **Research & Competitive Analysis** slide of your Module 6 final deck, alongside `competitive-and-journey.md`.

## Responses

- **Moment of misery / red flag #1:** Users trust off-platform channels more than the product. Dispatchers call their WhatsApp group "the real system," and 5 of 7 focus-group drivers carry a paper manifest in case the app crashes. When it does crash mid-route on Android 12/13, which happens on routes with roughly 40+ stops, drivers lose their remaining stops and spend about 20 minutes getting them read out by dispatch over the phone.

- **Moment of misery / red flag #2:** Feature bloat has buried the few actions drivers need most. "Start Route," used about 30 times a day, sits 2–3 levels deep. "Mark Delivered" takes 3 taps across 3 screens, often at a doorstep in bad weather with a package in hand. All 7 focus-group drivers said faster core actions matter more than any new feature, and new drivers describe the navigation as "menus inside menus."

- **Moment of misery / red flag #3:** Uploads and updates fail silently, so neither drivers nor dispatchers know what's real. About 35% of proof-of-delivery photo uploads fail on weak signal, with no retry and no confirmation, so drivers retake photos up to 3 times. Route changes take 8–15 minutes to reach drivers, with no push notification, so drivers keep following the old route. Status updates take 20–60 minutes to reach dispatch, which leaves dispatchers saying they "can't trust the board."

- **Product Health & Insights Summary (Claude's output):**

  > **Product Health & Insights Summary**
  >
  > **Scope:** 12 user research sessions (drivers, dispatchers, ops leadership) and 10 open bug reports
  >
  > **Executive Summary**
  >
  > The product's admin and reporting tools are a real strength and the main reason customers buy it, but frontline reliability has fallen to the point where users no longer trust it during live operations. Critical failures in route data (mid-route crashes, slow dispatch sync, no offline support) combine with a cluttered driver interface, so drivers face both "the app might fail" and "the app is slow to use even when it works." As a result, users across all roles now run parallel systems (WhatsApp groups, paper manifests, screenshots, phone calls to dispatch), which hurts adoption and has already put at least one enterprise renewal at risk.
  >
  > **Thematic Synthesis**
  >
  > **1. Technical Stability & Data Integrity**
  >
  > The most serious stability problem is that route data is lost while drivers are working. When the app crashes on longer routes, drivers lose their remaining stops and need dispatch to read them out by phone, costing about 20 minutes per incident. This failure explains much of the defensive behaviour seen in research: five of seven drivers in the focus group carry a paper manifest in case the app dies. Proof-of-delivery capture has the same problem of silent failure. Drivers can't tell whether an upload worked, so they repeat the action and lose confidence in the record.
  >
  > - **Critical:** The app crashes on Android 12/13 when a route has more than ~40 stops, and the remaining route is lost from the device. This hits high-volume drivers hardest.
  > - **High:** About 35% of proof-of-delivery photo uploads fail on weak signal, with no retry queue and no confirmation. Drivers retake photos up to three times.
  > - **High:** Low trust in the app has led to widespread fallback to paper manifests. This is a behavioural signal, not a single defect, but it is directly caused by the items above.
  >
  > **2. Platform Sync & Real-Time Coordination**
  >
  > Dispatchers and drivers each see a different, out-of-date version of the operation. Route changes take 8–15 minutes to reach drivers, and driver status changes take 20–60 minutes to reach the dispatcher dashboard. Neither side can rely on the system to coordinate in real time. Dispatchers describe an external messaging group as "the real system," which means the product has effectively been demoted to a record-keeping tool for its core coordination job.
  >
  > - **Critical:** Dispatch reassignments take 8–15 minutes to reach drivers, with no push notification, so drivers keep following the old route.
  > - **Medium:** Driver status changes take 20–60 minutes to appear on the dispatcher dashboard, and completed stops still show as "in progress." Dispatchers report they "can't trust the board."
  > - **High:** Coordination has moved to off-platform channels (WhatsApp, texts, phone calls). This is a cross-cutting result of both sync failures.
  >
  > **3. Field Connectivity & Offline Resilience**
  >
  > The app needs a constant connection, which doesn't match real field conditions, especially on rural routes. With no signal, the stop list doesn't load at all, so the product can't be used for part of the customer's territory. Drivers work around this by screenshotting their route every morning, a manual backup that doesn't update when the route changes.
  >
  > - **High:** Offline mode doesn't cache the stop list, so drivers see a blank route with no connection. This fully blocks work on rural and low-coverage routes.
  > - **High:** Weak-signal conditions also make the photo upload failures in Theme 1 worse, so connectivity gaps undermine both navigation and proof of delivery.
  >
  > **4. Discovery, Navigation & Core Workflow UX**
  >
  > The feedback here is the most consistent across roles: years of adding features have buried the few actions frontline users need. Features are added and almost never removed, so high-frequency actions like "Start Route" (used about 30 times a day) and "Mark Delivered" now sit two to three levels deep. Completing a delivery takes three taps across three screens, which is especially painful at a doorstep in poor weather with a package in hand. Leadership sees the commercial impact directly: frontline users "use maybe 5%" of the product and can't find it, and a simpler routing-focused competitor is being evaluated. All seven focus group drivers said speed of core actions matters more than any new feature.
  >
  > - **High:** "Mark Delivered" takes three taps across three screens, with no single-tap option. This is the top frontline complaint and a main reason drivers text dispatch instead.
  > - **High:** Core actions are buried two to three levels deep after recent feature additions, and the home screen can't be configured. Engineering rated this Medium, but research ties it directly to adoption problems and renewal risk.
  > - **High:** New drivers are overwhelmed by the menu structure ("menus inside menus") and can't become productive within a day. Key workflows such as reporting a failed delivery are hard to find.
  >
  > **5. Algorithmic Curation (Route Optimization)**
  >
  > Route optimization works in theory but ignores what drivers know on the ground. It doesn't account for long-standing road closures, live traffic, or site access details such as rear loading docks and one-way streets. There's also no way to save local corrections, so experienced drivers override the suggested route every day. Each manual override weakens the value of routing, which is the main capability competitors are offering.
  >
  > - **Medium:** Route optimization ignores road closures, traffic, and known access constraints, and local overrides can't be saved. Drivers repeat the same corrections daily.
  > - **Minor Technical Debt:** GPS pins drift by up to 200 m in dense urban areas, which triggers incorrect "arrived at stop" detection. The onboarding tutorial can't be reopened after first launch, and there's no in-app help for less common workflows such as reporting a failed delivery. Both are Low severity on their own but make the navigation problems in Theme 4 worse.

- **Did the AI catch the specific moment of misery / pain point you found in Step 1?:** Yes. It captured all three pain points, along with the workarounds users have adopted: WhatsApp and text coordination, paper manifests, route screenshots, and phone calls to dispatch. It kept the specific metrics too (35% upload failure, 8–15 minute sync lag, 3-tap delivery), so the misery stays concrete rather than abstract.

- **Did it smooth over a critical frustration into a generic bullet point?:** Mostly no. Each theme has clear, measurable examples and a severity rating. There are three exceptions:
  1. **The "Minor Technical Debt" catch-all** feels tacked on and plays down the issues inside it.
  2. **GPS drift is underweighted.** Pins drift up to 200 m and trigger false "arrived at stop" events. That's rated Low, but it directly feeds the data-integrity and "can't trust the board" problems.
  3. **The severities are inconsistent.** Driver-status sync lag is rated **Medium**, while the off-platform coordination it causes is rated **High**. The cause is ranked below its own effect.

- **Did the AI try to suggest features or a roadmap despite the constraints?:** Not explicitly. It made no recommendations and listed no features. It did frame several problems as a missing feature, though, which implies the fix (see Logic leak #1).

- **Logic leak / hallucination #1:** Soft roadmap leak. Several findings describe the absence of a specific feature instead of the user's problem:
  - "no single-tap option"
  - "home screen can't be configured"
  - "no retry queue"
  - "local overrides can't be saved"
  - "offline mode doesn't cache the stop list"

  Each one quietly prescribes a solution. For example, "drivers can't complete a delivery quickly at the doorstep" is the problem, and "single-tap delivery" is one possible solution. This framing pushes the team toward specific fixes before solutioning has started.

- **Logic leak / hallucination #2:** AI inference presented as finding. The AI added judgments that go beyond the source data:
  - It raised feature bloat from engineering's **Medium** rating to **High**.
  - It called routing "the main capability competitors are offering."
  - It described the product as "demoted to a record-keeping tool."

  These may be reasonable, but they are the AI's interpretations, not things users or bug reports stated. They should be labeled as synthesis or removed. I also checked the specific figures and claims against the 12 research sessions and 10 bug reports:
  - "5 of 7 drivers"
  - "~30 times a day"
  - "at least one enterprise renewal at risk"
  - "simpler competitor being evaluated"

  _[TODO: Fill in result — "All traced back to source" OR "X did not appear in the source data and was hallucinated."]_
