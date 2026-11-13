# Competitive Analysis & Journey Map

> **Module 2 · Lab 2 — ★ Deliverable 2.** Repo file `02-discovery/competitive-and-journey.md` — part of your submission.
> Do the lab in the **Module 2 · Exercise 2 Guide** (linked from the Module 2 deck), then click **⬇ Download .md** — it saves as this exact file. Commit it here.
> It becomes the **Competitive Analysis & Journey Map** slide of your Module 6 final deck. Builds on your `ai-synthesis.md` and your Module 1 `problem-hook.md`.

## Responses

- **Role, who are you solving for?:** A frontline delivery driver who runs 40+ stops a day and spends their whole shift in the RouteLogic mobile app.

- **Goal, what is this user ultimately trying to achieve?:** Get through every stop quickly and with confidence, without fighting the app at each doorstep.

- **Friction, the main barrier (moment of misery) stopping them:** Feature bloat has buried the actions drivers repeat all day. "Start Route" (about 30 uses a day) sits 2–3 levels deep, and "Mark Delivered" takes 3 taps across 3 screens, often in bad weather with a package in hand. All 7 focus-group drivers said core-action speed matters more than any new feature. Drivers text dispatch instead, and 5 of 7 carry a paper manifest in case the app crashes on long routes.

- **External tools the user is forced to use:** SMS/WhatsApp messages to dispatch; phone calls to dispatch; a printed paper manifest; phone screenshots of the route (camera roll); the driver's own memory of local roads and site access.

- **The process, the 3–5 manual steps they take:**
  1. **Before the shift:** At the depot, while there's signal, screenshot the stop list and keep a paper manifest in the cab as a backup if the app crashes or loses signal.
  2. **On the road:** Ignore parts of the optimized route and drive around known closures and access problems from memory, repeating the same corrections every day.
  3. **At the doorstep:** Skip the 3-screen "Mark Delivered" flow and text or WhatsApp dispatch to confirm the drop-off or report a failed delivery.
  4. **Proof of delivery:** Retake the photo up to 3 times, because about 35% of uploads fail on weak signal with no confirmation.
  5. **When the app fails:** If the app crashes or a route change comes in, switch to paper or screenshots and call dispatch to have the remaining stops read out, which takes about 20 minutes.

- **Core frustration, where the process feels most "broken":** The doorstep. The driver is holding a package, often in bad weather, and has to tap through three screens to mark one delivery, then can't tell whether the proof-of-delivery photo uploaded. At that point it's faster to send dispatch a text than to use the app, and from then on the app stops being the system of record.

- **The evidence, a quote or behavior from the research:**
  - **Behavior (complexity):** All 7 focus-group drivers said speed of core actions matters more than any new feature. "Mark Delivered" takes 3 taps across 3 screens, and drivers text dispatch instead.
  - **Quote (complexity):** New drivers describe the navigation as "menus inside menus." _[TODO: Swap in a direct driver quote about taps or buried actions if your research has one.]_
  - **Behavior (lost trust):** 5 of 7 drivers carry a paper manifest "just in case the app dies."
  - **Quote (cost of failure):** "The app crashed mid-route and lost my remaining stops. I had to call the office to read them to me off a screen. Twenty minutes gone."
  - **Quote (workaround):** "Route optimization sent me down a road that's been closed for months. It doesn't know about traffic or the loading dock round the back. I override it every day."

- **Journey map, a shareable link or the map file you committed:** [`02-discovery/journey-map.html`](journey-map.html). It maps one shift across five stages, covering the workaround, tools, emotional curve, driver quotes, severity, and cost at each stage, and marks the doorstep as the lowest point. Open the file in a browser to view it.
