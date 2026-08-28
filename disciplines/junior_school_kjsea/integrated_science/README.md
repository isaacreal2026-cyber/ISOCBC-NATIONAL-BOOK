# Junior School — Integrated Science

**Tier:** KJSEA (Grade 9) · **KJSEA paper codes:** `905/1` (theory), `905/2` (practical)
**Status:** ⬜ Room only. No strand map, no lessons.

## Scope note — this is not one subject

Integrated Science fuses what 8-4-4 split into separate primary science strands. Expect content drawn
across **Biology, Chemistry, Physics, and Agriculture/Health-related science**, integrated rather than
taught side by side.

That integration is the point, and it is also where the Senior School split happens: this is the last
time the learner meets science as one subject. In Grade 10 it fragments into Biology, Chemistry and
Physics as separate STEM electives.

**Series-level opportunity:** this is the subject where we can pre-teach the concepts that become the
Grade 10 Chemistry and Biology strands already mapped in
`disciplines/senior_school_pathways/STEM/`. Atoms, cells, states of matter, and simple machines all
start here.

## KJSEA profile

| Field | Value |
| --- | --- |
| Papers | `905/1` (theory), `905/2` (**practical**) |
| Weighting | 60% KJSEA + 20% SBA (Grades 7–8) + 20% KPSEA (Grade 6) — see `core_directives/assessment_logic.md` |
| Grading | 8 achievement levels → EE / ME / AE / BE |
| Placement role | Core signal for STEM pathway placement |

⚠ **Verify before drafting:** confirm the practical paper's format, the apparatus list, and the
strand/sub-strand structure from the KICD Grade 7–9 Integrated Science designs.

## What goes in this folder

```
integrated_science/
├── README.md
├── g7_STRAND_MAP.md           <- ⬜ to do
├── g8_STRAND_MAP.md           <- ⬜ to do
├── g9_STRAND_MAP.md           <- ⬜ to do   (KJSEA exam year)
├── practicals/                <- ⬜ to do   (905/2 — build this early, not late)
└── lessons/                   <- ⬜ to do
```

## Notes for MKUBWA

- **The practical paper is where BE learners leak marks**, because practicals are taught last, rushed,
  or skipped entirely by schools without apparatus. Build `practicals/` early and design every
  practical around **apparatus a real Kenyan junior school can obtain** — otherwise it is fiction.
- Never let an activity depend on a laboratory the school does not have. Local materials first.
- ⚠ **Safety register applies in full.** Any heating, glassware, chemicals, electricity, or specimen
  handling: flat, literal, imperative. No jokes. (See `core_directives/STYLE_GUIDE.md` §3.)
- **Don't teach a model as the truth.** Particles, circuits, and the Bohr-style atom all get patched at
  Senior School. Say so plainly, mark the deeper version `💡 Stretch`.
- Anchor everything. Junior schoolers need the physical thing before the term — a jiko, a sufuria,
  rusting iron sheets, a posho mill, charcoal, rain on a corrugated roof.

## Verification backlog

- [ ] Obtain KICD Grade 7, 8, 9 Integrated Science curriculum designs; record year + ISBN
- [ ] Confirm KJSEA `905/1` and `905/2` structure, apparatus list and practical format from KNEC
- [ ] Confirm approved textbook(s) and record in `curriculum_rules/source_mapping.json`
- [ ] Map Grade 9 concepts forward to the Grade 10 Chemistry / Biology strands we already hold
