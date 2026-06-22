# GEOM 2120 — Survey Computations Trainer

A small, gamified study tool for **BCIT GEOM 2120 (Pre-Entry Survey Computations)**.
It's a single self-contained `index.html` — no build, no dependencies, works fully
offline. Open it in any browser (or add it to your phone's home screen).

**Live:** https://kevingriffin-new.github.io/geom2120-trainer/

## What it covers

Modules 1–6, each with concept questions and hands-on **Step Drills**:

- **Module 1 — Units & Conversions:** gons ↔ degrees ↔ radians, DMS, interior vs
  exterior angle sums, legal/metric units.
- **Module 2 — Angles & Distances:** vertical/zenith angles (VA = 90° − ZA), reducing
  a slope distance to HD and ΔH, bearings (Whole Circle ↔ Quadrant).
- **Module 3 — Closed Traverse:** angle balancing, the Compass / **Bowditch** Rule
  corrections, sign-tracking on errors & corrections, and a guided closure walkthrough.
- **Module 4 — Alternate Traverses & Blunders:** the swing-angle method, and locating
  a single distance blunder.
- **Module 5 — Missing Parts & Resection:** three-point resection, and missing
  bearing/distance of a line.
- **Module 6 — Trigonometric Levelling:** short-line and reciprocal elevations, loop
  levelling closure, and long lines (curvature & refraction) with gradients.

## How it teaches

The design leans on two ideas from instructional practice:

- **Backward chaining (the "military" method):** each procedure is broken into tiny
  steps, and you drill them *back to front* — first you do only the **last** step
  (everything before it filled in), then the last two, then three… until you can run
  the whole thing cold. The end of a procedure gets the most practice, because that's
  the part furthest from a beginner's comfort.
- **Scaffold, then fade:** every step shows you exactly the data it needs (no
  recalling, no reverse-engineering). Support is meant to come off later, once the
  process is in your hands.

## Modes

- **📖 Watch & Learn** — a slow, plain-language walkthrough that fills a real traverse
  sheet one step at a time (the SW9 loop from the L3A notes).
- **🪜 Step Drill** — do it yourself, backward-chained, with a worksheet that builds up,
  hints, and a full "show me." Fresh random numbers every round.
- **Sequence It / Spot the Step / Work the Numbers** — order the steps, recall the
  formulas, and work the actual figures.
- **Final Prep** — everything across the modules shuffled together.

## Running it

Just open `index.html` in a browser. Progress (streak, best) is saved locally in that
browser. There's no server and nothing is collected.

## Status

A practice tool, not a promise — it's a place to do reps, not exam prep. Worked
examples and formulas come from the GEOM 2120 lecture material, and each drill's
generator is verified against the worked answers (e.g. every generated resection's
computed hub lands on the true point; loop corrections sum to the misclosure). Not an
official BCIT resource, and no affiliation with the course or instructor.
