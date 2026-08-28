# ROOM READINESS REPORT

**Generated:** 2026-08-28
**Repository:** `isaacreal2026-cyber/ISOCBC-NATIONAL-BOOK`
**Branch:** `arena/01a04848-isocbc-national-book`
**Scope:** Expansion to two national exam tiers — **KJSEA** (Grade 9) and **KCBE / Senior Secondary**
(Grade 12)

---

## Verdict: 🟡 THE ROOM IS BUILT —but it is not ready to write in yet

All five requested items are delivered. The structure, the assessment rules and the source registry
exist and are internally consistent.

**But readiness of the room is not the same as readiness to write.** Of the 20 subject-grades this
series now claims to serve, **2 are grounded in a verified source**. The rest are empty folders with
correct names. The two grounded ones are Grade 10 only — and **the KCBE exam is sat at Grade 12**.

Read §5 before you commission any content.

---

## 1. Folder structure — ✅ DELIVERED

| Requested | Created | Status |
| --- | --- | --- |
| `/disciplines/junior_school_kjsea` | ✅ | with 5 subject folders |
| `/disciplines/senior_school_pathways` | ✅ | with 3 cluster folders |
| `/core_directives/assessment_logic.md` | ✅ | 2 tiers, weightings, bands |
| `/curriculum_rules/source_mapping.json` | ✅ | 19 sources, valid JSON |
| Room Readiness report (root) | ✅ | this file |

### Discipline tree as built

```
disciplines/
├── README.md                        # tier explainer
├── junior_school_kjsea/             # TIER 1 — KJSEA, Grade 9
│   ├── english/                     #    901/1, 901/2
│   ├── kiswahili/                   #    902/1, 902/2
│   ├── mathematics/                 #    903
│   ├── integrated_science/          #    905/1, 905/2
│   └── social_studies/              #    907
└── senior_school_pathways/          # TIER 2 — KCBE, Grade 12
    ├── STEM/
    │   ├── chemistry/grade10/STRAND_MAP.md    🟡 migrated
    │   └── biology/grade10/STRAND_MAP.md      🟡 migrated
    ├── Social_Sciences/
    └── Arts_Sports/
```

### ⚠ One change you should know about: existing Grade 10 work was MOVED

The old `disciplines/grade10/{chemistry,biology}` sat outside the new two-tier structure and would have
become a competing third structure. It has been migrated:

```
disciplines/grade10/chemistry/STRAND_MAP.md
  →  disciplines/senior_school_pathways/STEM/chemistry/grade10/STRAND_MAP.md
disciplines/grade10/biology/STRAND_MAP.md
  →  disciplines/senior_school_pathways/STEM/biology/grade10/STRAND_MAP.md
```

Content is unchanged apart from a tier banner added at the top. Both files were untracked, so this was a
plain filesystem move with no history to preserve. Easy to revert if you disagree — say so now, before
content gets written into the new locations.

---

## 2. Subject clusters — ✅ DELIVERED (with a coverage gap)

### KJSEA tier — 5 of 10 examined subjects scaffolded

The 5 you asked for are in place. KJSEA also examines five more, which are **not** scaffolded:

| Scaffolded | Not scaffolded (but examined) |
| --- | --- |
| English (901) | **Agriculture & Nutrition** (906) |
| Kiswahili (902) | **Religious Education** — CRE (908) / IRE (909) / HRE (910) |
| Mathematics (903) | **Creative Arts & Sports** (911) |
| Integrated Science (905) | **Pre-Technical Studies** (912) |
| Social Studies (907) | **Kenya Sign Language** (904) |

Agriculture & Nutrition and Pre-Technical Studies both carry **practical/project papers**, which is
exactly the kind of content this series is good at. Recommend adding them.

### KCBE tier — 2 of ~30 pathway subjects scaffolded

- **STEM** — Chemistry and Biology at Grade 10 only. **13 further learning areas unscaffolded**,
  including **Physics**, which most STEM career tracks require.
- **Social Sciences** — empty. ~13 learning areas.
- **Arts & Sports** — empty. 5 learning areas.

**Physics is the single biggest subject gap.** Medicine, engineering and computing tracks all need it.

---

## 3. Assessment rules — ✅ DELIVERED

`core_directives/assessment_logic.md` defines both tiers.

### KJSEA — 60/40 ✅ as you specified, with one correction

Your 60/40 national-to-school-based ratio is right in substance. The official breakdown is finer, and
the file records both:

| Component | Weight | Nature |
| --- | --- | --- |
| KJSEA (Grade 9 national exam) | **60%** | National |
| SBA (Grades 7–8) | **20%** | School-based |
| KPSEA (Grade 6) | **20%** | **National** |

> ⚠ The "40% school-based" is a simplification: **20% of it is KPSEA, which is itself a national
> assessment** (sat at Grade 6). The file gives writers the honest phrasing to use with learners.
> Inside the project, "60/40" remains the working shorthand.

### Grading bands ✅ EE / ME / AE / BE

Eight achievement levels across four bands, with point scores:

| Band | Levels | Percentage | Points |
| --- | --- | --- | --- |
| **EE** | EE2 / EE1 | 90–100 / 75–89 | 8 / 7 |
| **ME** | ME1 / ME2 | 58–74 / 41–57 | 6 / 5 |
| **AE** | AE1 / AE2 | 31–40 / 21–30 | 4 / 3 |
| **BE** | BE1 / BE2 | 11–20 / 1–10 | 2 / 1 |

**The most important number in the table is 41%** — the AE→ME line. A learner at 35% is four percentage
points from being *competent* rather than *deficient*. That is the series' core promise.

### KCBE — 70/30 ⚠ PROVISIONAL

70% Grade 12 summative + 30% SBA (Grades 10–11). **This is widely reported but I could not confirm it
against a primary KNEC document.** It is flagged `provisional` in the assessment file and must not be
stated as settled fact in learner-facing print until verified.

### Legacy transition handled

KCPE last sat 2023; **KCSE last sat 2027** — both systems are live right now. The file carries a hard
rule: never print an 8-4-4 letter grade (A, B+, C−, E) in CBE content. The scales are not convertible.

Two consequences for the book business, both recorded in the rules:
- **Grade 9 is the KJSEA exam year** — but 40% of the score was already banked before it.
- **Grades 10 and 11 bank 30% of a certificate**, not of a report.

---

## 4. Source mapping — ✅ DELIVERED

`curriculum_rules/source_mapping.json` — **valid JSON, 19 sources, all cross-references resolve.**

| Status | Count | Meaning |
| --- | --- | --- |
| `verified` | **2** | Confirmed directly against the primary PDF |
| `provisional` | 3 | Credible secondary sources; not yet primary-confirmed |
| `unverified` | 14 | Placeholders — title/ISBN unknown |

**Verified (inspected the documents myself):**
- KICD Grade 10 Chemistry · 2024 · **ISBN 978-9914-52-913-5** — 3 strands / 8 sub-strands / 180 lessons
- KICD Grade 10 Biology · 2024 · **ISBN 978-9914-52-915-9** — 3 strands / 10 sub-strands / 180 lessons

**Deliberately not verified: the KLB titles.** I did not invent them. The MKUBWA persona's core job is
translating KLB-grade prose, so identifying the actual KLB senior school Chemistry and Biology books is
a **blocking** task — but guessing an ISBN would put a wrong number in a printed book. Those entries are
`unverified` with `null` fields.

The registry also enforces precedence: **KICD designs outrank textbooks.** Where KLB and KICD disagree,
the design wins.

---

## 5. What is NOT ready — read before commissioning content

### 🔴 Structural gaps (will break the series if ignored)

1. **Grades 11 and 12 do not exist in any form.** KCBE is sat at Grade 12 and its SBA comes from Grades
   10–11. A Grade 10-only series is a series with no exit exam. **This is the biggest gap in the repo.**
2. **Physics is entirely absent** from STEM, despite being required by most STEM careers.
3. **Social Sciences and Arts & Sports are empty clusters.**

### 🟡 Verification gaps (must clear before drafting)

4. **The two Grade 10 strand maps have open backlogs.** Verbatim Key Inquiry Questions and Specific
   Learning Outcomes are still unconfirmed for most sub-strands. Drafting against partial outcomes risks
   teaching the wrong scope.
5. **The KCBE 70/30 split is unconfirmed** against a primary KNEC source.
6. **The achievement-level band boundaries are unconfirmed** against a primary KNEC source (they are
   mutually consistent across secondary reports, which is why they are `provisional`, not `unverified`).
7. **KLB textbook titles are unidentified.**
8. **Grade 10 Chemistry strand 3.0 Organic Chemistry** is listed with 8 lessons but **no numbered
   sub-strands** in the design. Confirm before inventing structure.

### ⚪ Capacity gaps

9. **`assets/diagrams/` is empty.** The Science, Geography and Arts & Sports content all need diagrams.
   Arts & Sports especially cannot be written without notation, choreography and staging assets.
10. **Arts & Sports has an unresolved rights question** — music, choreography, scripts and film extracts
    may carry copyright or cultural-heritage restrictions. Resolve before embedding third-party material.

---

## 6. What changed in existing files

| File | Change |
| --- | --- |
| `disciplines/grade10/**` | **Moved** into `senior_school_pathways/STEM/` (see §1) |
| `core_directives/KICD_CHECKLIST.md` | Change-control step now also updates `source_mapping.json` |
| `agents/prompts/writer.md` | Loads both tier paths + `assessment_logic.md`; exam tier is now a required input |
| `README.md` | Rewritten for the two-tier structure |
| `AGENTS.md` | Filled in — was an empty stub |
| `.gitignore` | Properly populated — was an empty stub |
| `.cursorignore`, `.env.template` | Created (previous turn) |

---

## 7. Recommended order of work

| # | Task | Why now |
| --- | --- | --- |
| 1 | Confirm or revert the Grade 10 migration (§1) | Everything else depends on where files live |
| 2 | Verify the KCBE 70/30 split and the grading bands from primary KNEC documents | Every lesson states these numbers |
| 3 | Source KICD Grade 11 and 12 designs for Chemistry and Biology | Without these there is no KCBE product |
| 4 | Identify and register the KLB senior school titles | MKUBWA cannot translate a book we haven't named |
| 5 | Clear the verbatim-outcome backlogs on the two Grade 10 maps | Cheap, and unblocks drafting immediately |
| 6 | Source the KICD Physics design | Largest subject gap in STEM |
| 7 | Add the 5 unscaffolded KJSEA subjects, starting with Agriculture & Nutrition and Pre-Technical Studies | They carry practical papers we are well suited to |
| 8 | Stand up diagram production | Blocks Science, Geography and Arts & Sports |

---

## 8. Confidence statement

- **Structure:** high confidence — delivered exactly as specified, with the one migration flagged in §1.
- **KJSEA 60/40:** high confidence — consistent across KNEC guidance and independent reporting.
- **Grading bands:** medium-high — consistent across reports, not yet primary-confirmed.
- **KCBE 70/30:** **medium** — widely reported, not primary-confirmed. Treat as provisional.
- **KLB titles:** **none** — deliberately left blank rather than guessed.

Sources are cited inline in `core_directives/assessment_logic.md` §8 and per-entry in
`curriculum_rules/source_mapping.json`.
