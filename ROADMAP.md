# Step-Drill Roadmap — Modules 3, 4, 5

Goal: extend the **Step Drill** (backward-chained micro-steps + scaffolded givens)
across the whole course, at the same grain as the Module 3 *Angle Balancing* drill
(5 micro-steps, 5 rungs, "what you're given" panel, fresh random numbers).

## The reusable pattern (every phase ships this)
- **Atomic micro-steps** — one calculation per screen, never a "jump".
- **Backward-chaining ladder** — Rung 1 = last step only (rest given); add one step at the
  front each rung until the whole phase runs cold.
- **Givens panel** — always shows the data + constants needed for *this* step (n, start bearing,
  the leg's distance, etc.). No recalling, no reverse-engineering.
- **Hint + "Show me"** — Show me works the actual numbers, including DMS carries.
- **Generator** — produces clean problems that always close (like the angle generator that
  always sums to exactly 540°). *This is the main correctness work per phase.*
- **Scaffold → fade** — after all rungs cleared, unlock "off-book" rounds: givens collapse to
  the minimum, then vanish, then reproduce from the figure.

## Two axes of backward chaining
1. **Over operation-steps** — Phases 1, 4, the resection, missing-parts (a fixed recipe).
2. **Over legs/rows** — Phases 2, 3, coordinate accumulation: "do the LAST leg, then the last
   two, …". Mirrors walking the traverse and gives the same easy-first-win momentum.

---

## MODULE 3 — Closed Traverse (the backbone)

| Phase | Micro-steps (the grain) | Ladder | Givens panel | Traps to hint |
|---|---|---|---|---|
| **1 · Angle balancing** ✅ built | Σ angles → (n−2)·180 → misclosure → correction = −e/n → apply +c | 5 rungs (over steps) | n, the 5 raw angles | the 720°/540° rule; sign of correction |
| **2 · Forward bearings** | start bearing given → next = prev + balanced∠ − 180° (±360 to stay 0–360) → repeat per leg → closing check (returns to start bearing) | over legs (last leg first) | start bearing, balanced angles | +180 vs −180; staying in 0–360; DMS carry |
| **3 · Latitudes & departures** | per leg: ΔE = d·sin(brg); ΔN = d·cos(brg) | over legs | each leg's bearing + distance | ΔE=sin / ΔN=cos swap; sign by quadrant |
| **4 · Misclosure & precision** | ΣΔE → ΣΔN → eE → eN → er = √(eE²+eN²) → RP = Σs/er (round) | 6 rungs (over steps) | the ΔE/ΔN columns, Σs | loop ⇒ eE=ΣΔE; RP as a 1:n ratio |
| **5 · Adjust & coordinates** | factor = −e/Σs → per-leg adj = factor·d → adjusted ΔE/ΔN → accumulate E,N station by station → confirm last = start | over legs (final station first, watch it close) | factors, distances, ΔE/ΔN, start coords | proportional-to-distance; the closure payoff |
| **Link add-on** (slots before Phase 1) | initial bearing by inverse → final bearing by inverse → e = Σβ − n·180 − (af−ai) | 3 rungs | the two known baselines | quadrant of the inverse; the (af−ai) term |
| **Full-traverse "campaign"** | chains Phases 1→5 on ONE problem, end to end | the ultimate front-to-back run | fades as you go | — |

## MODULE 4 — Alternate Traverses & Blunders (heavy reuse of M3)

| Phase | Micro-steps | Notes |
|---|---|---|
| **A · Loop w/ known baseline** | reuse 1–5, but misclosure = ΣΔE − (En−Ei), ΣΔN − (Nn−Ni); + initial bearing by inverse | small add-on drills, not a rebuild |
| **B · Two known points (swing angle)** | assume start bearing → bearings (Ph2) → ΔE/ΔN (Ph3) → assumed end-bearing = atan(ΣΔE/ΣΔN) → true end-bearing by inverse → swing = assumed − true → rotate ALL bearings → recompute → compass adjust (Ph5) | new skill = swing angle; rest reused |
| **C · Single angular blunder** 🔍 | recompute misclosure → forward open-traverse coords → reverse (angle′=360−angle, from reversed final bearing) → reverse coords → compare each station fwd vs rev → the matching station is the culprit | "detective" format — momentum from the mystery, not the math |
| **D · Single distance blunder** 🔍 | confirm angles OK → recompute eE,eN → bearing of error = atan(eE/eN)+quadrant → er = √(eE²+eN²) → match to a leg's bearing (±180°) → blunder ≈ er | same detective payoff |

## MODULE 5 — Missing Parts & Resection

| Phase | Micro-steps | Priority |
|---|---|---|
| **H · Three-point resection** (the A5 type) | inverse → a, c, angle B → (A+C)=360−(X+Y+B) → k → A, C → B1, B2 → sine law AP, CP → coords from A → check from C | **HIGH** — it's the assignment; ~8 steps, ladder ends on the self-check |
| **E · Missing bearing & distance, one line** | bearings consistent? → ΔE,ΔN of each known leg → ΣΔE,ΣΔN → missing ΔE=−ΣΔE, ΔN=−ΣΔN → bearing=atan(ΔE/ΔN)+quadrant → distance=√(ΔE²+ΔN²) | HIGH — close cousin of Ph3 + closure-to-zero |
| **F · Two missing distances** | set up the two closure eqns → trig-identity solution for sk, sn | LOW (niche, algebra-heavy) |
| **G · Two missing bearings (Shifting Line)** | assume start (0,0) → open traverse → closing-line brg/dist → distance-distance intersection (cosine law) → the two bearings | MED (geometric, advanced) |

## MODULE 6 — Trigonometric Levelling (NEW — L6A / A6)

Heights from zenith angles + slope distances. Core equation: **ΔH = Hi + SD·cos(ZA) − Ht**,
then **Elev_B = Elev_A + ΔH**. (ZA = *zenith* angle, so cos; ZA>90° ⇒ negative ⇒ downhill.)

| Phase | Micro-steps (the grain) | Ladder | Givens | Traps |
|---|---|---|---|---|
| **J · Short-line elevation** | SD·cos(ZA) → ΔH = Hi + SD·cos(ZA) − Ht → Elev_B = Elev_A + ΔH | 3 rungs (over steps) | Hi, Ht, SD, ZA, Elev_A | cos of *zenith* angle; sign when ZA>90°; +Hi −Ht |
| **K · Reciprocal (fwd + rev)** — *A6 Q1* | **Opt 1 (Hi=Ht):** mean ZA = (ZA_AB + 180° − ZA_BA)/2 → mean SD → Elev_B = Elev_A + SD_mean·cos(ZA_mean). **Opt 2 (Hi≠Ht):** ΔH_AB → ΔH_BA → mean ΔH = (ΔH_AB − ΔH_BA)/2 → Elev_B | over steps | both ZA/SD, Hi/Ht per end, Elev_A | the mean-ZA formula; DON'T average ZA/SD when Hi≠Ht; sign on reverse |
| **L · Closed-loop elevation closure** | ΔH per leg → ΣΔH (→0) = misclosure → ΣHD → adj/leg = −(ΣΔH/ΣHD)·HD → adjusted ΔH → accumulate elevations → close | over legs | legs' ΔH + HD, start elev | **same shape as the M3 traverse closure** — instant familiarity/momentum |
| **M · Long line (c−r) + gradient** — *A6 Q2* | long line? (>300 m) → (c−r) = 0.0675·D²(km) → ΔH = Hi + SD·cos(ZA) − Ht + (c−r) → Elev (may be multi-leg) → gradient = ΔElev/HD × 100%, vs 2% limit | over steps | ZA/SD, Hi/Ht, D, elevs, 0.0675 | **D in km**; (c−r) always ADDED (up & downhill); gradient as % |

Concept MCQ: the 3 levelling types (differential/trig/barometric); short vs long (≈300 m boundary);
why simultaneous-reciprocal cancels curvature & minimises refraction; (c−r) ≈ 0.0675·D²km and always +.

**Big reuse win:** Phase **L** is the *elevation* version of the M3 closure he already drilled
(misclosure → distribute by distance → accumulate → close) — cheap to build, high momentum.

---

## Suggested build order
1. **M3 Ph2 (bearings)** — continues straight from angle balancing.
2. **M3 Ph3 (lat/dep)** → **Ph4 (misclosure/precision)** → **Ph5 (adjust/coords)** + full-traverse campaign.
3. **M5 Ph H (resection)** — highest exam value; bring forward if the final weights it.
4. **M4 Ph C/D (blunders)** — the detective format is the most engaging; great for momentum.
5. **M6 Ph J + K (short-line + reciprocal)** — small, self-contained, covers A6 Q1; good standalone momentum builder.
6. **M6 Ph L (loop elevation closure)** — nearly free, reuses M3 closure machinery.
7. **M5 Ph E (missing parts basic)**, **M6 Ph M (long line + gradient, A6 Q2)**.
8. **M4 Ph B (swing)**, **M5 F/G**, **link add-on** — as time allows.

After ~steps 1–2 the engine is fully reusable, so each later phase is mostly a generator +
a micro-step list, not new machinery.
