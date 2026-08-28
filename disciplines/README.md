# `disciplines/` — the two national exam tiers

Everything we write is aimed at one of Kenya's two national assessment tiers. Pick the tier first; it
determines the assessment weightings, the grading bands, the source designs, and the shelf life of the
content.

```
disciplines/
├── junior_school_kjsea/        # Tier 1 — KJSEA, sat at Grade 9
│   ├── english/
│   ├── kiswahili/
│   ├── mathematics/
│   ├── integrated_science/
│   └── social_studies/
│
└── senior_school_pathways/     # Tier 2 — KCBE, sat at Grade 12
    ├── STEM/
    │   ├── chemistry/
    │   └── biology/
    ├── Social_Sciences/
    └── Arts_Sports/
```

## The two tiers at a glance

| | **Tier 1 — KJSEA** | **Tier 2 — KCBE** |
| --- | --- | --- |
| Full name | Kenya Junior School Education Assessment | Kenya Certificate of Basic Education |
| Sat at | End of **Grade 9** | End of **Grade 12** |
| Replaces | KCPE (last sat 2023) | KCSE (last sat **2027**) |
| National : school-based | **60 : 40** | **70 : 30** |
| First cohort | 2025 | **2028** |
| Decides | Senior School pathway placement | University / TVET placement + certification |
| Grading | 8 achievement levels → 4 bands (EE/ME/AE/BE) | 8 achievement levels → 4 bands (EE/ME/AE/BE) |

Full rules, weightings and band tables: `core_directives/assessment_logic.md`.

## Legacy warning — we are mid-transition

KCPE is gone (last sat 2023). **KCSE is still running and its last sitting is 2027.** Both systems are
live right now, and they use *different* grading scales — 8-4-4 used a 12-point letter scale (A–E),
CBE uses the 8-level / 4-band scale.

**Rule:** ISOCBC writes **only** for the CBE tiers. Never mix 8-4-4 letter grades (A, B+, C−) into
learner-facing text. If a learner asks "what grade is 62%?", the answer is achievement level, not a
letter.

## Cluster structure (senior school)

Senior School learners take **seven learning areas**: four compulsory (English, Kiswahili/KSL,
Community Service Learning, Physical Education) plus three from their chosen pathway.

- **STEM** — Mathematics, Biology, Chemistry, Physics, General Science, Agriculture, Computer Studies,
  Home Science, and the technical subjects. Currently scaffolded: Chemistry, Biology at Grade 10.
- **Social_Sciences** — Advanced English, Literature, History & Citizenship, Geography, Business
  Studies, Religious Education, foreign and indigenous languages. Not yet scaffolded.
- **Arts_Sports** — Sports & Recreation, Physical Education, Music & Dance, Theatre & Film, Fine Arts.
  Not yet scaffolded.

## Where content lives

```
<tier>/<cluster>/<subject>/<grade>_STRAND_MAP.md
```

The `STRAND_MAP.md` for a subject-grade is the **single source of truth** for what we are required to
teach: strands, sub-strands, KICD learning outcomes, key inquiry questions, and the lesson budget.
Drafted lessons sit alongside it.
