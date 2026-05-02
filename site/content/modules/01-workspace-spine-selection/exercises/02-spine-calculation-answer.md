---
title: "Model answer: Exercise 2 — Spine Calculation and Spec Card"
type: answer
weight: 21
draft: false
---

## The worked solution

Here is the complete worked example for the build parameters: 40 lb bow / 28-inch AMO {{< gloss "Draw length" "draw length" >}} / 100-grain field point / 11/32-inch {{< gloss "Port Orford cedar" "Port Orford cedar" >}}.

### Step 1 — Rose City chart result

*Chart result: 50–55#*

The Rose City chart for a 40 lb recurve or longbow at 28 inches with 100-grain points recommends approximately 50–55# {{< gloss "Static spine" "static spine" >}} for a wood arrow shaft.

The "naturally fixed spine" note means you do not order by spine number — you order by **shaft diameter and density grade**. The 11/32-inch diameter, combined with the wood's natural density, will fall within a range. When you receive the batch, you spine-sort them individually and select the shafts that fall in your target range for the matched set. Shafts outside the range become spares or get returned. This is why you order 26–28 shafts for a 24-arrow set.

*What this means for ordering:* Specify "11/32-inch Port Orford cedar, spine-sorted 50–55#" when ordering from a supplier who pre-sorts by {{< gloss "Spine" "spine weight" >}} (Rose City and 3Rivers Archery both offer sorted batches). If ordering unsorted, buy more and measure yourself.

### Step 2 — Stu Miller calculator result

For 40 lb / 28 inch draw / 100 gr point / recurve bow type, Stu Miller's calculator typically returns approximately **50–52#**. For a longbow input (which places the arrow further from the bow centerline, requiring a slightly different paradox correction), it may return **52–55#**.

*Calculator result example: 51# (recurve) / 53# (longbow)*

**Do they agree?** Yes, within the margin of the calculation. The chart returns a range (50–55#); the calculator returns a single point estimate. When they agree within 5#, you have high confidence in the range. Use the **50–55# range** as the purchase spec.

When they diverge by more than 5–10#: trust the calculator for your specific parameters. The chart is a two-variable lookup ({{< gloss "Draw weight" "draw weight" >}} + draw length only); the calculator accounts for point weight, shaft length, and bow type. If you change point weight from 100 gr to 125 gr, the calculator will shift the recommendation toward 45–50# (heavier point = more bend force = need stiffer shaft). The chart won't capture that shift.

*PFF note:* The default PFF of 1.0 is the correct starting point. A clean, consistent finger release gives approximately PFF 1.0; a strong "pluck" release may require PFF 0.9 or lower (your release adds effective draw weight). Calibrate after you have arrows flying.

### Step 3 — Per-inch adjustment worked example

At **28 inches (working default):** no adjustment. Target spine: **50–55#**.

If draw length turns out to be **29 inches:** add 5 lb. Target: **55–60#**. Why? A longer arrow has more distance over which to flex. The same bow energy applied to a longer lever produces more bending. To counteract that additional flex and keep the arrow recovering cleanly through {{< gloss "Archer's paradox" "archer's paradox" >}}, you need a stiffer shaft — and in the AMO convention, stiffer = higher number.

If draw length turns out to be **27 inches:** subtract 5 lb. Target: **45–50#**. A shorter arrow has less lever arm, flexes less, and needs a less stiff shaft to bend correctly at your lower draw weight.

*One-sentence explanation:* A longer draw length produces a longer arrow, which bends more easily under the same bow force — to keep {{< gloss "Dynamic spine" "dynamic spine" >}} constant, you compensate by choosing a stiffer static spine (higher AMO number), so the arrow bends the right amount rather than too much.

### Step 4 — Completed spec card

```
ARROW SPEC CARD — MATCHED SET
==============================
Date: [today's date]

Shaft material:  Port Orford cedar (POC)
Shaft diameter:  11/32"

Draw weight:     40 lb (measured at 28 inches AMO)
Draw length:     28 inches  [ default — to be confirmed by measurement ]
Point weight:    100 grains (glue-on field point)

Rose City chart spine:   50–55#
Stu Miller spine:        51# (recurve) / 53# (longbow)
Purchase spine target:   50–55#

Batch quantity to order: 27 shafts  (24 finished + 3 culls = 27 total)
Shaft length to order:   32 inches  (29" cut length + ~1" taper allowance + margin)

Left-hand shooter:       YES
Feather wing:            LEFT-WING
Fletch profile:          Shield cut
Fletch offset:           Left offset (2–3 degrees)
Feather count:           3
```

## Why these choices

**Why order 27 shafts for a 24-arrow set?** Cedar spine is a natural property — even within a "spine-sorted" batch, you will find 2–4 shafts that are borderline, visibly curved, or have grain runout that makes them poor candidates for a matched set. Ordering the culls margin up front means you finish with 24 good arrows rather than 20 good arrows and 4 compromises.

**Why order at 32 inches when the draw length is 28?** Arrow length is not draw length. The shaft extends from the nock groove to the {{< gloss "Point taper" "point taper" >}} — you add approximately 1 inch for the taper at the front end, plus you want to be able to cut the arrow to the correct length in module 2 after straightening, which may involve trimming a bent section off the front end. 32 inches gives you 3 inches of working margin.

**Why use the range (50–55#) rather than the calculator's single point (51#) as the purchase spec?** Because spine-sorted cedar batches are sold in 5# increments (45–50#, 50–55#, 55–60#). The calculator gives you a point estimate as a reference; the chart's range maps directly to how suppliers sell batches. The two tools together confirm you are in the right 5# bracket.

## Common pitfalls

**Pitfall 1 — Confusing AMO wood spine notation with modern decimal notation.** AMO 50–55# means "stiffness equivalent to a 50 to 55 pound draw weight." A higher AMO number is stiffer. In modern carbon/aluminum decimal notation (e.g., Easton 500, 400), a lower number is stiffer. If you are cross-referencing a carbon arrow chart while working on cedar, you are comparing different systems. Do not mix them.

**Pitfall 2 — Using the Stu Miller calculator without specifying bow type.** "Recurve" and "longbow" inputs produce different results because the two bow designs have different {{< gloss "Bow window" "bow window" >}} depths and different paradox behavior. A traditional longbow with no shelf cutaway places the arrow further from the bow centerline, requiring more paradox flex — which means the same draw weight longbow may need a slightly different spine than a recurve. Know which you have.

**Pitfall 3 — Leaving the draw length as "default 28 inches" and never measuring.** The per-inch rule is ±5 lb per inch — a 2-inch error in draw length is a full 10# error in spine selection, which is the difference between arrows that fly cleanly and arrows that fishtail badly. Measure your draw length before placing the shaft order. The simplest method: nock an arrow, draw to your anchor point, and have a partner mark the shaft at the front of the bow. Measure from the mark to the nock groove. That is your arrow length — subtract about 1 inch for the point taper to get an approximate draw length.
