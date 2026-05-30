---
name: carlisle-moore-design
description: Use this skill to generate well-branded interfaces and assets for Carlisle Moore Architects, either for production or throwaway prototypes/mocks/etc. Contains essential design guidelines, colors, type, fonts, assets, and UI kit components for prototyping a warm editorial residential-architecture brand.
user-invocable: true
---

Read the README.md file within this skill, and explore the other available files.

Key files:
- `README.md` — brand context, content fundamentals, visual foundations, iconography.
- `colors_and_type.css` — all design tokens (`--rust`, `--ink`, `--paper`, type families) + helper classes. `@import` it or copy it; it pulls the Adobe Fonts kit.
- `site.css` — the full production stylesheet from the live website, for reference.
- `assets/` — logos, house mark, and project photography (`assets/photos/`).
- `ui_kits/website/` — reusable JSX components (nav, slideshow, editorial body, fee table, footer) recreating the website surface.
- `preview/` — small specimen cards.

If creating visual artifacts (slides, mocks, throwaway prototypes, etc), copy assets out and create static HTML files for the user to view. If working on production code, copy assets and read the rules here to design fluently in this brand.

Design principles to honor: a single rust/terracotta accent on cream paper; warm brown inks; five typefaces each with a fixed role (Aviano Sans labels, Columbia Titling caps, URW Antiqua body + italic headlines, Franklin Gothic numerals); square corners and no drop shadows; thin hairline rules and a 40×2px rust bar as structure; uppercase Titling captions separated by middots; no emoji.

If the user invokes this skill without other guidance, ask them what they want to build or design, ask a few questions, and act as an expert designer who outputs HTML artifacts _or_ production code, depending on the need.
