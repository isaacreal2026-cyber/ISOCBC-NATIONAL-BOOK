# Senior School — Social Sciences Pathway

**Tier:** KCBE (Grade 12) · **Grades:** 10, 11, 12 · **Cluster:** Social Sciences
**Status:** ⬜ Room only. No strand maps, no lessons.

## Learning areas in this pathway

From the KICD Grade 10 design's proposed subject list:

| | Learning area | Scaffolded here? |
| --- | --- | --- |
| 22 | Advanced English | ⬜ |
| 23 | Literature in English | ⬜ |
| 24 | Indigenous Language | ⬜ |
| 25 | Kiswahili Kipevu / Kenya Sign Language | ⬜ |
| 26 | Fasihi ya Kiswahili | ⬜ |
| 27 | Sign Language | ⬜ |
| 28 | Arabic | ⬜ |
| 29 | French | ⬜ |
| 30 | German | ⬜ |
| 31 | Mandarin Chinese | ⬜ |
| 32 | History and Citizenship | ⬜ |
| 33 | Geography | ⬜ |
| 34 | Christian / Islamic / Hindu Religious Education | ⬜ |
| 35 | Business Studies | ⬜ |

## Differentiation note — this pathway is not uniform

Unlike STEM, where the four core sciences share a mindset, this cluster contains three genuinely
different kinds of subject, and they cannot share a lesson template unchanged:

1. **Languages** (Advanced English, Kiswahili Kipevu, Fasihi, Arabic, French, German, Mandarin,
   Indigenous Languages, Sign Language) — skills-accumulation subjects. Progress is measured in
   production (speaking, writing, comprehension), not in topic coverage. Drill, register, and
   cultural context matter more than sequence.
2. **Humanities** (History and Citizenship, Geography, Religious Education) — content-plus-evidence
   subjects. Structure beats recall: chronology, causation, source evaluation, spatial reasoning.
3. **Business Studies** — applied-procedural. Definitions, documents, and worked transactions.

**Rule:** write each group's lesson template separately. Do not force a Chemistry-style strand map
onto a language.

## Sharing with the other tiers

English and Kiswahili appear at **both** tiers — as KJSEA subjects at junior school
(`disciplines/junior_school_kjsea/`) and as *differentiated* Senior School subjects here (Advanced
English, Kiswahili Kipevu, with two extra lessons). They are **related but not the same course**; keep
the content separate and cross-reference deliberately.

## Structure

```
Social_Sciences/
├── languages/          ⬜ to do   (one subfolder per language)
├── humanities/         ⬜ to do   (history, geography, RE)
└── business_studies/   ⬜ to do
```

Proposed — confirm the grouping before creating subject folders, so we do not encode a guess.

## Notes for MKUBWA

- **Handle politics, ethnicity, religion, land and historical grievance with care.** Be accurate,
  balanced and age-appropriate. Where interpretations are contested, say they are contested rather than
  picking a side. This series must be safe to hand to any Kenyan child.
- **Values are real content here**, not decoration — patriotism, social justice, integrity, unity.
  Per `STYLE_GUIDE.md` §1: reason with the reader, never moralise at them.
- **Content rots.** Names and dates are the weakest thing to drill. Teach structure first.
- **Data and map skills are the highest-yield repair area** across Geography and History: it is a
  transferable skill, it appears every year, and it is routinely under-taught.

## Verification backlog

- [ ] Confirm the KICD Grade 10–12 designs for each subject; record year + ISBN per subject
- [ ] Confirm which subjects have published designs at all (KICD has been rolling these out in stages)
- [ ] Decide and record the sub-grouping for this cluster
- [ ] Record approved textbook(s) in `curriculum_rules/source_mapping.json`
