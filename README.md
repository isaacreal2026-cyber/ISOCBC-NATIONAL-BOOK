# ISOCBC NATIONAL BOOK

A KICD-compliant book series for Kenya, covering **both national exam tiers**, written for the learner
who has been told they are not good at this subject.

**Series premise:** this reader is not lazy and not slow. They are *under-translated* — nobody ever
converted the textbook's language into theirs. Our job is translation, not simplification.

**Tone:** an older sibling who already fought this exam and came back with the strategy guide.
> Internal shorthand for that voice is **"God-Mode"** — a learner-facing power register. It is a
> *narrative frame*, not a claim about cheating, and it never touches lab safety.

---

## The two tiers we write for

| | **Tier 1 — KJSEA** | **Tier 2 — KCBE** |
| --- | --- | --- |
| Sat at | End of **Grade 9** | End of **Grade 12** |
| Replaces | KCPE (last sat 2023) | KCSE (last sat **2027**) |
| National : school-based | **60 : 40** | **70 : 30** *(provisional)* |
| First cohort | 2025 | 2028 |
| Decides | Senior School pathway placement | Certification + university/TVET placement |

Both tiers grade on **8 achievement levels across 4 bands: EE / ME / AE / BE.** We take a learner at
BE/AE and aim for **ME as the floor, EE as the aim**. Full rules: `core_directives/assessment_logic.md`.

⚠ **Never mix grading systems.** 8-4-4 used letter grades (A–E); CBE uses achievement levels. No letter
grades anywhere in learner-facing content.

---

## Status

🟡 **The room is built. Two of twenty subject-grades are grounded.**

| Area | State |
| --- | --- |
| Monorepo + two-tier structure | ✅ done |
| Assessment rules (KJSEA 60/40, KCBE 70/30, EE/ME/AE/BE) | ✅ done |
| Source registry (`curriculum_rules/source_mapping.json`) | ✅ done (2 verified / 14 unverified) |
| Writer persona (MKUBWA) | ✅ done |
| Grade 10 Chemistry + Biology strand maps | 🟡 mapped, verbatim checks outstanding |
| Junior school (KJSEA) content | ⬜ none |
| Grade 11–12 content | ⬜ none — **KCBE is sat at Grade 12, this is the biggest gap** |
| Diagrams | ⬜ none |

Full audit: **[`ROOM_READINESS.md`](ROOM_READINESS.md)**.

---

## Layout

```
core_directives/                    # The law. Read before writing.
├── STYLE_GUIDE.md                  # Older-sibling voice, God-Mode register, Translation Protocol
├── KICD_CHECKLIST.md               # CBC compliance: strands, outcomes, competencies, PCIs, rubrics
└── assessment_logic.md             # KJSEA + KCBE: weightings, grading bands, legacy transition

curriculum_rules/
└── source_mapping.json             # Registry of approved KICD designs / KLB books + status

agents/prompts/writer.md            # MKUBWA — the lesson-writing persona

disciplines/
├── junior_school_kjsea/            # TIER 1 — KJSEA (Grade 9)
│   ├── english/          (901/1, 901/2)
│   ├── kiswahili/        (902/1, 902/2)
│   ├── mathematics/      (903)
│   ├── integrated_science/ (905/1, 905/2)
│   └── social_studies/   (907)
└── senior_school_pathways/         # TIER 2 — KCBE (Grade 12)
    ├── STEM/
    │   ├── chemistry/grade10/STRAND_MAP.md   🟡 180 lessons, 8 sub-strands
    │   └── biology/grade10/STRAND_MAP.md     🟡 180 lessons, 10 sub-strands
    ├── Social_Sciences/            ⬜ room only
    └── Arts_Sports/                ⬜ room only

assets/diagrams/                    # Committed diagram exports + naming/alt-text rules
```

## Where the rules come from

Content is grounded in the official **KICD curriculum designs**, registered with edition year and ISBN in
`curriculum_rules/source_mapping.json`. Currently verified:

- Grade 10 Chemistry — KICD, June 2024 · ISBN 978-9914-52-913-5
- Grade 10 Biology — KICD, June 2024 · ISBN 978-9914-52-915-9

⚠ KICD rationalises designs year on year. **Never draft against an unverified source**, and never invent
an ISBN — unknown fields stay `null`.

## Setup

```bash
cp .env.template .env      # then fill in. .env is gitignored — never commit it.
```

## How to write a lesson

1. Read `core_directives/STYLE_GUIDE.md`, `KICD_CHECKLIST.md` and `assessment_logic.md`.
2. Load `agents/prompts/writer.md` (MKUBWA) into your agent of choice.
3. Pick an unstarted sub-strand from the relevant tier strand map.
4. Give MKUBWA the input contract from §6 of the persona file — **including the exam tier**.
5. Do not merge until all three checklists pass: KICD §8, Style Guide §8, and the tier's assessment rules.

See `AGENTS.md` for the full agent rulebook.

## Order of authority

1. **Safety** — absolute. Flat, literal, never joked about.
2. **KICD compliance** — the design outranks any textbook, including KLB.
3. **Style / voice**
4. **Momentum**
