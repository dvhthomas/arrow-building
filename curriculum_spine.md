---
topic: "Traditional wood target arrows — building, tuning, and maintenance"
slug: "traditional-wood-arrows"
goal: "Build, tune, and maintain ~24 beautiful traditional wood target arrows from parts. Be competent enough to assemble from parts, fletch, repair (broken arrows / tips / feathers), and tune to my bow. Teaching others is a future goal, not a near-term test."
tested_via:
  - personal_confidence
  - practitioner_conversation
audience_starting_point: "Has done this before but it's been a while. Owns all the tools (fletching jig, taper tool, dip tube, etc.) but they aren't currently set up. Self-described visual learner — wants strong photos / diagrams / Wikimedia Commons / NPS / public-domain / Creative Commons imagery. High-fidelity AI-generated imagery acceptable as a fallback only when free-use coverage is genuinely thin."
depth_vs_breadth: "deep"
validation_preferences:
  - scenario
timeline: "a few weeks"
tools_present:
  - fletching_jig_offset_clamp
  - taper_tool
  - dip_tube
  - owns_bow_40lb_draw
  - draw_length_unknown_default_28in
hue: 90
font_preset: "book"
running_example:
  name: "The matched set: 24 Port Orford cedar arrows, 11/32\", 100 gr field points, shield-cut left-wing 3-fletch, for a 40 lb left-handed bow"
  description: "Every module is anchored to this specific build. The learner selects shafts for this bow (40 lb at AMO 28\", adjusted if actual draw length differs), straightens and tapers all 24, seals and crests them as a batch, fletches with left-wing natural turkey shield-cut feathers using the offset clamp, attaches 100-grain glue-on field points and plastic nock inserts, then tunes and repairs within the same set. By the end the learner holds all 24 finished arrows and has shot a bareshaft group confirming the spine match."
  introduced_in_module: 1
module_count: 5
glossary_seed:
  - term: "Spine"
    definition: "The measured stiffness of an arrow shaft; properly matched spine allows the arrow to flex correctly around the bow riser and recover to straight flight downrange."
  - term: "Dynamic spine"
    definition: "The effective stiffness of an arrow during the actual shot — how it actually bends and recovers as it accelerates off the bow. Dynamic spine is influenced by shaft length, point weight, draw weight, bow design, and release style, and is what truly determines whether an arrow flies well."
  - term: "Port Orford cedar"
    definition: "Chamaecyparis lawsoniana, a Pacific Northwest softwood regarded as the premier natural material for traditional arrow shafts. Valued for its consistently straight grain, high strength-to-weight ratio, and superior modulus of elasticity — it recovers quickly from the flex of the shot and returns to straight flight faster than most alternatives."
  - term: "GPI (grains per inch)"
    definition: "A weight-per-unit-length specification for arrow shafts, calculated as shaft weight in grains divided by shaft length in inches. Port Orford cedar at 11/32-inch diameter typically runs 10–15 GPI. GPI is used to compare shaft weights independently of length."
  - term: "Archer's paradox"
    definition: "The phenomenon in which an arrow shot from a traditional bow — where the arrow must be offset to one side of the riser — nonetheless flies straight to the target because it flexes around the bow and recovers to the line of flight as it leaves the string. Correct spine matching is essential for this recovery to happen properly."
  - term: "Bareshaft tuning"
    definition: "A tuning method in which one or more unfletched (bare) shafts are shot alongside fletched arrows at the same aiming point. Where the bare shaft impacts relative to the fletched group reveals spine match (horizontal deviation) and nocking point position (vertical deviation) before feather corrections can hide errors."
  - term: "Feather fletching"
    definition: "Natural feathers (typically turkey) used as arrow vanes. Feathers collapse on contact with the bow shelf and recover instantly, making them the preferred choice for off-the-shelf shooting on traditional bows. The rough side of the feather faces outward on the arrow shaft."
  - term: "Dip tube"
    definition: "A length of PVC or metal tube long enough to fully submerge an arrow shaft. Used with liquid finishes (gasket lacquer, shellac, polyurethane) to coat the entire shaft in a single smooth, even pass. Multiple dip coats — with light sanding between — produce a durable moisture barrier."
---

# Spine narrative

## Module count

The interview specifies `deep` depth and `a few weeks` timeline. The R29 default table gives 5 modules for that cell. Five modules is the correct count here — deep means fewer, richer modules rather than a survey across more topics. No deviation from the table default.

## Sequencing rationale

The concept_map in research.yaml establishes clear hard dependencies. The five modules follow this chain:

1. **Workspace and spine selection** — All of draw weight, draw length, static spine, dynamic spine, AMO standard, archer's paradox, and the Stu Miller calculator must come before any shaft is touched. This is also where the learner's tools get set up after years of disuse — the interview explicitly flags "tools owned but not set up" as the starting condition. Workspace first is non-negotiable.

2. **Shafts: selection, straightening, tapering** — Wood species choice, shaft straightening, point taper, and nock taper all depend on knowing what spine you're targeting (module 1). GPI and GPP belong here because the weight-matching exercise for 24 shafts is the first real batch operation in the build. Footing is covered as a named concept with a contrast (it is *not* part of the canonical build path for this curriculum, but a practitioner must know what it is and when it's warranted).

3. **Sealing, cresting, finishing** — Depends on all shaft-prep concepts from module 2. The dip tube workflow is the central skill; cresting is optional but covered because the matched-set goal has an aesthetic dimension and the learner specifically asked for visual identification across the batch.

4. **Fletching, nocks, and points** — Depends on sealed, prepped shafts from module 3. Feather wing direction (left-wing for a left-handed shooter), shield-cut profile with offset clamp, nock insert installation, and field point attachment. FOC calculation belongs here because it is only meaningful once all components are on the arrow and their weights are known.

5. **Tuning, maintenance, and repair** — Depends on completed arrows from module 4. Bareshaft tuning is the primary method; paper tuning and walk-back tuning are contrasted. Repair workflows (nock, point, fletching, shaft) round out the practitioner competency.

## Pedagogy ordering applied

Within each module, the brief's `driving_question` follows the question-first pattern: start with a problem the learner's current state cannot yet solve, then answer it. Each module accumulates on the matched set — by module 5 the learner has 24 finished arrows in hand and is shooting groups to verify the build.

## Running example

The running example is declared explicitly in the spine frontmatter: **"The matched set: 24 Port Orford cedar arrows, 11/32", 100 gr field points, shield-cut left-wing 3-fletch, for a 40 lb left-handed bow."** Every brief and every module the builders produce must anchor exercises and scenarios to this specific set. The example name is short enough to use inline without awkwardness.

## Open questions resolved

The research.yaml open_questions flagged several unknowns (draw weight, draw length, handedness, jig model, point weight, shaft diameter). All are resolved by the interview answers provided to the designer:

- Draw weight: 40 lb at AMO 28" (default; learner must be taught how to adjust if actual draw length differs)
- Draw length: unknown, AMO 28" used as working default
- Handedness: left-handed → left-wing feathers, left-helical or left-offset clamp geometry
- Jig: fletching jig with offset clamp (not full helical) — shield-cut three-fletch with offset is the canonical path
- Point weight: 100 grain glue-on field points
- Shaft: 11/32" Port Orford cedar

## Contrast discipline

Every brief includes a contrast whose `when_alternative_wins` is honest and non-trivial. The interview explicitly called out two contrasts to include: (1) carbon vs wood for competitive 3D, and (2) parabolic vs shield for beginner form. Both appear in the relevant briefs. No brief has a contrast where the alternative loses on every dimension.

## Visual learner note for module builders

The audience is a self-described visual learner. Every brief's `exercise_goal` includes `[TODO: embed ...]` markers calling for labeled diagrams, photographs, or public-domain illustrations. Module builders must prioritize Wikimedia Commons, NPS, and manufacturer educational-page imagery before falling back to AI-generated art. When AI-generated imagery is used, it must be labeled as such in the module.
