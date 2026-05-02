---
title: "Model answer: GPI sort and batch-tracking table"
type: answer
weight: 10
draft: false
---

## The worked solution

Here is what a correctly completed batch session looks like, using a realistic sample batch. Your numbers will differ, but the pattern and decisions should match.

**Scale preparation:**

Zero the scale with nothing on the pan. If your scale has a tare button, press it and confirm "0.0" before each shaft. If it does not auto-tare, confirm the empty-pan reading is consistent (the same non-zero value every time) and subtract that value from every measurement.

**Length measurement:**

Lay a rigid rule alongside the shaft with one end flush with the point tip. Read at the nock tip. Alternatively, mark the endpoint on a flat table and measure the gap. Either method is fine as long as you use the same method for every shaft.

**Sample GPI calculations — 10 shafts from a realistic bundle:**

| Shaft # | Weight (gr) | Length (in) | GPI |
|---------|------------|-------------|-----|
| 1 | 285.0 | 30.5 | 9.3 |
| 2 | 299.5 | 30.5 | 9.8 |
| 3 | 302.0 | 30.5 | 9.9 |
| 4 | 307.5 | 30.5 | 10.1 |
| 5 | 311.0 | 30.5 | 10.2 |
| 6 | 313.5 | 30.5 | 10.3 |
| 7 | 316.0 | 30.5 | 10.4 |
| 8 | 320.5 | 30.5 | 10.5 |
| 9 | 335.0 | 30.5 | 11.0 |
| 10 | 358.5 | 30.5 | 11.8 |

From this sample, the cluster runs from 9.8 to 10.5. A center value of 10.2 GPI with a ±1.0 GPI window (keep range 9.2–11.2) retains shafts 1–9. Shaft 10 at 11.8 GPI is a CULL-WEIGHT. That is one cull from ten shafts — within the expected 5–15% band.

**Choosing the center value:**

The temptation is to choose the midpoint of your full range. Don't — choose the center of the largest cluster. If most of your shafts run 10.0–10.8 GPI and one outlier is 8.5 and one is 12.2, your center is around 10.4, not 10.35. The two outliers are culls regardless.

**Status column entries for the sample:**

- Shafts 1–9: KEEP (pending straightness check)
- Shaft 10: CULL-WEIGHT

## Why these choices

**Why ±1 GPI tolerance, not tighter?**

±1 GPI on 11/32-inch cedar corresponds to roughly ±10 grains on a 300-grain shaft — about ±3%. At target distances up to 30 yards, that weight spread introduces maybe 1–2 inches of elevation difference at the far end, which is small enough that form variation dominates. A tighter window (±0.5 GPI) is possible if your scale resolution is good and your bundle is cooperative, but it costs you more culls and may not produce a measurable accuracy improvement on foam targets.

**Why not weigh the whole finished arrow and sort by total arrow weight instead?**

You could, but GPI sorting happens before tapering, sealing, or component installation. GPI lets you make the weight-match decision with raw shafts, before you invest labor in them. Sorting by total finished weight requires building all 28 arrows first — that is the wrong order.

**Why convert length to decimal inches rather than fractions?**

The division step (weight ÷ length) is much easier with decimals. 30 3/8 inches as 30.375 divides cleanly; doing the arithmetic in fractions introduces error. Write fractions in your table if that's easier for measurement, then convert once for the GPI calculation.

## Common pitfalls

**Pitfall 1: Not zeroing the scale between shafts.**

If your scale drifts or accumulates error, a reading of "303.0" on shaft 5 may actually be 300.5 gr with 2.5 gr of drift. Zero before every measurement, or at minimum every five shafts. A 2-grain error on a 300-grain shaft changes GPI by 0.07 — not catastrophic, but it can push a borderline shaft the wrong way.

**Pitfall 2: Measuring the shaft diagonally instead of axially.**

If the shaft is not perfectly parallel to the ruler when you measure length, you'll get a number that's slightly too long. Even a 5-degree angle adds less than 0.4% error on a 30-inch shaft, so this matters only at high precision — but parallel is still the right habit.

**Pitfall 3: Choosing a tolerance window first, then sorting to fit it.**

The correct sequence: measure all 28 shafts, *then* look at the distribution, *then* choose the center value and window. Choosing ±1 GPI before you see the data can lead to a window that excludes most of your shafts if the bundle ran heavier or lighter than expected. Let the data show you where the cluster is, then draw the window around the cluster.
