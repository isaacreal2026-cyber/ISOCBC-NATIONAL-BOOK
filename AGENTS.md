# AGENTS.md — instructions for coding/AI agents in this repository

## What this repository is

A Kenyan educational book series (ISOCBC NATIONAL BOOK): KICD-compliant Senior School / Junior School
content written in an "older sibling" voice for learners currently scoring **Below** or **Approaching**
Expectation, aimed at **Meeting Expectation as the floor and Exceeding Expectation as the aim**.

It is **content**, not application code. There is no build step, no dependency tree, and no test suite.
Treat Markdown and JSON as the source of truth.

## Read these before doing anything

| Order | File | Why |
| --- | --- | --- |
| 1 | `core_directives/STYLE_GUIDE.md` | The voice. Older sibling, God-Mode register, Translation Protocol. |
| 2 | `core_directives/KICD_CHECKLIST.md` | Compliance gate. Strands, outcomes, competencies, PCIs, rubrics. |
| 3 | `core_directives/assessment_logic.md` | The two exam tiers (KJSEA, KCBE), weightings, grading bands. |
| 4 | `curriculum_rules/source_mapping.json` | Which KICD designs / KLB books are approved, and their status. |
| 5 | `agents/prompts/writer.md` | The MKUBWA lesson-writing persona. |

## Repository layout

```
core_directives/            The law. STYLE_GUIDE, KICD_CHECKLIST, assessment_logic
curriculum_rules/           source_mapping.json — registry of approved KICD/KLB sources
agents/prompts/writer.md    MKUBWA persona
disciplines/
  junior_school_kjsea/      Tier 1 — KJSEA (Grade 9)
    english/ kiswahili/ mathematics/ integrated_science/ social_studies/
  senior_school_pathways/   Tier 2 — KCBE (Grade 12)
    STEM/ Social_Sciences/ Arts_Sports/
assets/diagrams/            Committed diagram exports (see its README)
```

## Hard rules

1. **Safety outranks everything.** Never joke in, or adjacent to, a laboratory, chemical, fieldwork,
   apparatus or physical-training instruction. Safety language is flat, literal and imperative.
2. **Compliance outranks voice.** A funny lesson that misses a KICD learning outcome is a defect.
3. **Truth outranks momentum.** You may slow down; you may not simplify into falsehood.
4. **Never invent a source.** No guessed ISBNs, no invented curriculum outcomes, no fabricated quotes
   attributed to a textbook. Unverified metadata is `null`, and its status is `unverified`.
5. **Never mix grading systems.** CBE uses 8 achievement levels / 4 bands (EE, ME, AE, BE). 8-4-4 used
   A–E letters. Never print an 8-4-4 letter grade in learner-facing content.
6. **Dignity is non-negotiable.** Never write "weak", "slow", "remedial", "dull" or similar. A grade is
   a starting stat, never an identity.
7. **Never teach cheating.** Strategy, recall and exam technique are fine. Shortcuts around integrity
   are not.

## Working conventions

- **Strand maps are the source of truth for scope.** Draft from the map; never invent scope.
- **Nothing is drafted against a `status: "unverified"` source** in `curriculum_rules/source_mapping.json`.
- **Record the edition** (year + ISBN) of any design you work from, in both the strand map and
  `source_mapping.json`.
- **Diagrams** follow `assets/diagrams/README.md`: SVG, kebab-case, versioned, with alt text.
- **Secrets never enter the repo.** `.env` is gitignored; `.env.template` is the committed surface.
- **Don't commit generated output.** `_output/`, `_drafts/`, `_export/` are gitignored.

## Git

- Work is committed on the session branch and merged to `main` via pull request. **Do not force-push.**
- Commit message prefixes: `content:`, `rules:`, `structure:`, `kicd-sync:`, `fix:`, `docs:`.
  Example: `structure: add KJSEA and KCBE tier folders`
- KICD design revisions get their own PR: `kicd-sync: <subject> <grade> (<year> edition)`.

## Before you finish a task

- [ ] Re-read `core_directives/STYLE_GUIDE.md` §8 pre-ship checklist
- [ ] Re-read `core_directives/KICD_CHECKLIST.md` §8 per-lesson checklist
- [ ] Confirm the exam tier and its assessment rules were applied
- [ ] Confirm every source you cited is registered in `curriculum_rules/source_mapping.json`
- [ ] Confirm no secret, `.env`, or large binary was written into the repo
