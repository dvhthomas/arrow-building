# Review: traditional-wood-arrows

Generated: 2026-05-01T00:00:00-06:00
Mode: full
Modules reviewed: 5
Mechanical fixes applied: 2
Substantive flags: 7 (7 unapproved, 0 approved-pending-apply, 0 applied)

---

## Mechanical fixes

- **all modules**: Glossary merged — 59 terms written to `site/content/glossary.md` (3 conflicts surfaced separately as flags 1–3).
- **all modules**: Glossary auto-link pass completed — 223 `{{< gloss "..." >}}` shortcodes injected across 35 pages (module `_index.md`, exercises, validation, and answer files). The linker is idempotent; re-running is safe.

No frontmatter sync mutations were applied. The `check-frontmatter.sh` and `check-adjacency.sh` scripts reported missing `index.md` files (not `_index.md`). The builder produced Hugo section files (`_index.md`), which is correct for Hugo section bundles. The script expected bare `index.md` leaf bundles. This is a script/builder convention mismatch — see flag 4 below. No frontmatter content was changed.

---

## Script findings

- **adjacency**: `ok: false` — 5 `missing-page` entries. The script looks for `index.md`; the builder produced `_index.md` (Hugo section bundles). No actual adjacency chain errors were found — all five `prior_ends_with` / `next_expects` pairs are coherent across modules.
- **frontmatter**: `ok: false` — same root cause as adjacency (script cannot locate `_index.md` files to compare against briefs). No content-level frontmatter mismatches found on manual inspection.
- **urls**: 10 checked / 0 unhealthy. All brief reading URLs returned HTTP 200.
- **ai-prose**: 0 hits.
- **glossary**: 59 terms merged, 3 definition conflicts (see flags 1–3), 0 missing references.
- **citations**: all 5 modules above threshold (threshold: 4 inline footnotes). Counts: 01: 17, 02: 9, 03: 8, 04: 7, 05: 10.

---

## Substantive flags

### 1. glossary: "Bareshaft tuning" — minor typo in research.yaml canonical definition

```yaml
id: 1
approved: null
module: "(glossary — research.yaml)"
category: glossary_conflict
detail: |
  Two definitions exist. The research.yaml canonical definition contains a typo:
  "unfletched" is spelled "unfleteched" (transposed 'e').

  research.yaml: "one or more unfleteched (bare) shafts..."
  research.yaml spine seed (curriculum_spine.md): "one or more unfletched (bare) shafts..."

  The merge script logged this as a conflict between research.yaml and the
  "spine" source. Both are from the same document family; the typo is the only
  real difference. The merged glossary.md will carry whichever definition the
  merge script selected (it selected research.yaml as authoritative by source
  priority).
suggested_fix: |
  In research.yaml, line 98, change "unfleteched" to "unfletched".
  Then re-run merge-glossary.sh to regenerate glossary.md.
```

---

### 2. glossary: "Hot-melt adhesive" — substantive definition divergence between modules 4 and 5

```yaml
id: 2
approved: null
module: "04-fletching-nocks-points / 05-tuning-maintenance-repair"
category: glossary_conflict
detail: |
  Module 4 defines hot-melt adhesive as a thermoplastic (EVA) and explicitly
  states it is "not appropriate for nock installation." Module 5 defines it more
  narrowly as "a low-temperature formulation for archery use" applied in "solid
  stick or pellet form" and says nothing about the nock-installation caveat.

  Module 4 definition is more complete and correct for this curriculum. The
  module 5 definition omits the critical safety/technique distinction
  (hot-melt vs. nock cement) that module 4 establishes. The merged glossary.md
  will carry one definition; the omission in module 5 is the problem.

  Both definitions agree on the core function (thermoplastic, bonds on cooling,
  releases with heat, used for field points).
suggested_fix: |
  Accept the module 4 definition as canonical. In
  modules/05-tuning-maintenance-repair/new_terms.yaml, replace the Hot-melt
  adhesive definition with the module 4 text, or remove it entirely so the
  research.yaml / module 4 definition wins. No prose change in the module 5
  page body is needed — the page uses the term correctly.
```

---

### 3. glossary: "Nock cement" — substantive definition divergence between modules 4 and 5

```yaml
id: 3
approved: null
module: "04-fletching-nocks-points / 05-tuning-maintenance-repair"
category: glossary_conflict
detail: |
  Module 4 defines nock cement as "flexible adhesive... Remains flexible after
  cure to absorb repeated impact... Functionally interchangeable with fletching
  adhesive (e.g., Fletch-Tite)... distinct from hot-melt."
  Module 5 defines it as "adhesive specifically formulated for bonding... holds
  firmly under string-impact vibration while remaining removable with moderate
  heat. Bohning Fletch-Tite is the most widely cited example."

  Key divergence: module 5 says nock cement is "removable with moderate heat."
  Module 4 says it is distinct from hot-melt specifically because hot-melt
  releases with heat. If nock cement is also heat-removable, the distinction
  module 4 draws loses its meaning. This is a substantive inconsistency that
  could confuse a learner trying to decide which adhesive to use.

  The practical reality: Bohning Fletch-Tite is NOT heat-removable in the same
  sense as hot-melt — it is a water-based adhesive that bonds mechanically and
  is removed by peeling after applying gentle heat to soften the bond interface,
  not by melting. Module 5's phrasing implies a heat-release mechanism similar
  to hot-melt, which is misleading.
suggested_fix: |
  In modules/05-tuning-maintenance-repair/new_terms.yaml, revise the Nock cement
  definition to remove "removable with moderate heat" and instead say something
  like: "holds firmly under string-impact vibration; removed by peeling after
  heat-softening the bond — distinct from hot-melt, which melts to a liquid on
  heating."

  Then re-run merge-glossary.sh.
```

---

### 4. build_failure: scripts expect index.md; builder produces _index.md

```yaml
id: 4
approved: null
module: "(all — structural)"
category: build_failure
detail: |
  check-adjacency.sh and check-frontmatter.sh both report 5 "missing-page"
  errors because they look for:
    site/content/modules/<slug>/index.md
  The builder correctly produced Hugo section bundle files:
    site/content/modules/<slug>/_index.md

  This means the scripts cannot validate any module-level frontmatter or
  adjacency chain content for this curriculum. The check results are vacuous:
  "ok: false" because the files aren't where the scripts look, not because
  anything is actually wrong.

  On manual inspection, all five _index.md files have coherent frontmatter
  (title, weight, driving_question, contrast table, prior_ends_with,
  next_expects, date, draft: false) and the adjacency chain is logically sound.
suggested_fix: |
  Update check-adjacency.sh and check-frontmatter.sh to look for _index.md
  (Hugo section bundle convention) in addition to or instead of index.md.
  This is a plugin script bug, not a curriculum content bug.
```

---

### 5. contrast: module 03 — comparison table missing an "alternative wins" row

```yaml
id: 5
approved: null
module: "03-sealing-cresting-finishing"
category: contrast
detail: |
  The tapered shaft vs. parallel shaft comparison table (6 rows) does not
  contain a row where the alternative (parallel shaft) wins with bold emphasis
  in the cell. The "When it wins" information exists in prose below the table
  and is noted in the "Nock damage recovery" and "Custom taper control" rows,
  but no row is formatted as "When alternative wins" with the bold-highlight
  pattern used consistently in modules 01, 02, 04, and 05.

  Modules 01, 02, 04, and 05 all include at least one explicitly bolded
  "When the alternative wins" row in their comparison tables. Module 03's table
  has the information but does not surface it in the same emphasized row format,
  making the contrast feel incomplete by the curriculum's own standard.
suggested_fix: |
  Add a dedicated bolded row to the module 03 contrast table:
  | **When parallel shaft wins** | — | **Nock-end damage recovery: remove the
  damaged inch, re-taper, re-seat a new nock. No refinishing the whole shaft.
  Right choice for high-volume shooting where nock-end splits are common.** |
```

---

### 6. brief_contradiction: two [TODO] markers remain in module 03 prose body

```yaml
id: 6
approved: null
module: "03-sealing-cresting-finishing"
category: brief_contradiction
detail: |
  Two [TODO] tags are present in the published module 03 page body that signal
  unresolved builder decisions:

  1. Line 80 (after the dipping sequence step 7):
     "[TODO: learner fills in coat count recommendation from the ArcheryTalk
     thread before proceeding — the thread distinguishes 2-coat utility finish
     from 3-coat show finish]"

  2. Line 140 (after the drying/curing timeline table):
     "[TODO: learner confirms these values against the specific product's
     technical data sheet — temperature and humidity shift all of these numbers,
     and a cold garage in spring may require 2× the 'dry to touch' time]"

  These are not <!-- HTML comment --> style builder markers (which would not
  render in Hugo), but bare [TODO] text that will render visibly in the
  published site. They appear to be editorial notes left in the content
  accidentally.
suggested_fix: |
  For TODO 1: The prose above the tag already states "Two coats of shellac or
  gasket lacquer is the minimum for a target arrow used on foam or burlap
  targets." The TODO can simply be removed — the answer is in the preceding
  sentence.

  For TODO 2: Either remove the note (the table values are already sourced) or
  convert it to a proper callout block:
  > **Note:** Drying times vary significantly with temperature and humidity.
  > A cold or humid workspace may require 2× the times listed. Always verify
  > against your specific product's technical data sheet before re-coating.
```

---

### 7. definition_drift: module 03 GPP target range conflicts with research.yaml

```yaml
id: 7
approved: null
module: "03-sealing-cresting-finishing"
category: definition_drift
detail: |
  research.yaml defines GPP target as "6.5–8 GPP" for a midweight traditional
  arrow. Module 03 reproduces this correctly in the stated target range
  ("6.5–8 GPP" at line 102).

  However, module 03's worked example shows the matched set at "10.3–11.9 GPP"
  at 40 lb draw and notes this is "well above the 6.5 GPP floor, which means
  the matched set is safely in the mid-to-heavy traditional range."

  The numbers are internally consistent (413–477 grains ÷ 40 lb = 10.3–11.9),
  but the result is substantially outside the stated 6.5–8 GPP canonical range.
  The prose dismisses this with "well above the 6.5 GPP floor" without
  acknowledging that 10.3–11.9 GPP is also well above the 8 GPP ceiling of the
  stated target range.

  A 40 lb bow shooting 450–520 grain arrows at 10.3–11.9 GPP is in the
  heavy-arrow range, not the "mid-to-heavy" range implied. For a target archer
  (vs. a hunter), this may affect trajectory noticeably at longer distances.
  The research.yaml canonical range (6.5–8 GPP) and the BobLeeBows citation
  both cite 6.5–8 as the target — the module's result being 25–50% over the
  ceiling warrants an explicit acknowledgment rather than a quiet pass.
suggested_fix: |
  In the module 03 GPP section, add a clarifying note after the worked example:
  "The 10.3–11.9 GPP result places this matched set above the 6.5–8 GPP
  'midweight' range cited in most target-archery references. At 40 lb and
  indoor/close-range distances (under 20 yards), the heavier arrow is not a
  problem — it produces quieter bow noise and a slightly more forgiving release.
  At longer target distances (30–60 yards) the heavier arrow will have more arc.
  If flat trajectory at longer range matters, consider lighter shafts (9–10 GPI)
  or a lighter point (75–85 gr)."
```

---

## Notes on Module 5 bareshaft table

The explicitly-inverted bareshaft impact table for a left-handed archer (flag: none) was reviewed and found internally consistent:

- The flowchart and the table both state: bare shaft RIGHT = spine too stiff; bare shaft LEFT = spine too weak.
- The prose spine-adjustment section is consistent: "Left-handed: bare shaft lands RIGHT (stiff) — add heavier points."
- The footnote citation from Archery360 states "Reverse for left-handed archers" explicitly.
- Vertical readings (HIGH/LOW) are correctly noted as handedness-independent.

No error was found. The inversion is correct and self-consistent. No flag raised.
