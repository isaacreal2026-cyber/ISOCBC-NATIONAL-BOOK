# Diagrams

Every figure used by the ISOCBC series lives here, as **one source of truth** referenced from lessons
rather than pasted inline.

## Status

No diagrams produced yet. This folder is reserved and tracked so the pipeline has somewhere to write.

## Naming convention

```
<subject>_g<grade>_s<strand>-<sub-strand>_<slug>_v<version>.<ext>
```

Examples:

```
chemistry_g10_s1.4_ionic-lattice_v1.svg
chemistry_g10_s1.5_period3-trends_v2.svg
biology_g10_s1.3_plant-cell_v1.svg
biology_g10_s3.3_respiratory-surface_v1.svg
```

- **Lowercase kebab-case slugs.** No spaces, no capitals, no dates.
- **`v<version>` starts at `v1`** and increments for substantive redraws. Never overwrite an existing
  version — a lesson may pin an older one.
- **Preferred format: SVG.** Editable, scales, prints cleanly, diffs in Git. Raster only for photographs
  (`.jpg` / `.png`), and never as the master of a line drawing.
- Retired diagrams move to `_archive/`, they are not deleted (a lesson may still pin them).

## Every diagram must ship with

1. **The file itself** — clean lines, labelled parts, legible at A5 print size.
2. **A caption** — one sentence saying what the figure shows.
3. **A "what to notice" line** — the single thing the student must see, or the diagram is decoration.
4. **Alt text** — a full text equivalent (see rule below; meaning must never live in colour alone).
5. **Labels in the exam's own wording** — if the examiner wants "cell surface membrane", the label says
   "cell surface membrane", not "skin of the cell".

## Alt-text rule

Alt text must make the diagram **fully usable by a learner who cannot see it**: name every labelled
part, state the relationships between them, and state the point the figure proves.

> Bad: `alt="cell diagram"`
> Good: `alt="Labelled plant cell showing cell wall, cell surface membrane, cytoplasm, nucleus, large
> central vacuole and chloroplasts. The chloroplasts sit in the cytoplasm and are the site of
> photosynthesis; the vacuole is large and central, which is what makes the nucleus appear pushed to
> one side."`

## Style

- **Never encode meaning in colour alone.** Pair colour with a label, a pattern, or a shape.
- Consistent legend and scale conventions across a subject.
- Line weights and type sizes that survive A5 print and photocopying — assume the school photocopier is
  old and the toner is low.
- Kenyan context where honest: label local specimens and apparatus a Kenyan school actually has.

## Source files

Editable masters (`.excalidraw`, `.ai`, `.psd`, `.fig`, raw photo originals) go in `_source/` and are
**gitignored** — only the exported diagram is committed. See `.cursorignore` and `.gitignore`.

```
assets/diagrams/
├── README.md
├── _source/          # gitignored — editable masters
├── _archive/         # retired versions, still pinnable
└── <diagram files>
```
