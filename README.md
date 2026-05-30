# Carlisle Moore Architects — Design System

A warm, editorial brand system for **Carlisle Moore Architects**, a residential
architecture firm in **Mountain Brook, Alabama**. The identity reads like a
finely-printed monograph: terracotta "rust" ink on cream paper, classical
titling capitals, italic serif headlines, and large architectural photography
framed by thin rules.

This system was extracted from the firm's multi-page website (a process-driven
portfolio: *Introduction → Schematic → Development → Drawings → Administration →
Fees → Contact*). Every token, type role, and component below is lifted directly
from that built site.

---

## Index — what's in this folder

| Path | What it is |
|------|------------|
| `README.md` | This file — context, content + visual foundations, iconography |
| `colors_and_type.css` | All design tokens (CSS custom properties) + helper classes |
| `site.css` | The full production stylesheet from the live site (reference) |
| `assets/` | Logos (`logo-wordmark.png`, `logo.png`), house mark (`house.png`), divider, and project photography under `assets/photos/` |
| `preview/` | Specimen cards shown in the Design System tab |
| `ui_kits/website/` | High-fidelity recreation of the website surface as reusable JSX components |
| `SKILL.md` | Makes this folder usable as a downloadable Agent Skill |

The five brand typefaces are served from the firm's **Adobe Fonts (Typekit)**
kit: `https://use.typekit.net/wup0iix.css`. `colors_and_type.css` imports it.

---

## Brand context

Carlisle Moore Architects designs custom homes and renovations. The website is
organized around the firm's **design process** rather than a project gallery —
each page is a "plate" in a numbered sequence, presented like leaves of an
architectural folio. The featured project throughout is **The Borden Residence**.

The tone is unhurried, craft-forward, and quietly confident. The firm wants to
feel like a trusted collaborator, not a high-volume builder.

---

## CONTENT FUNDAMENTALS

**Voice.** Warm, literate, and measured. Speaks *to* the client ("Our process
begins with you") while keeping a curatorial third-person distance for captions
and labels. Never salesy, never breathless. Sentences are complete and softly
formal — closer to a letter than a brochure.

**Casing.**
- **Micro-labels, eyebrows, nav, folios** → ALL CAPS with wide letter-spacing
  (e.g. `PLATE 01 · OUR PROCESS`, `MOUNTAIN BROOK, ALABAMA`).
- **Headlines** → sentence case, set in *italic serif* ("The drawings that build
  the house").
- **Body** → ordinary sentence case.
- **Names / labels** → ALL CAPS in the Aviano display face ("THE LIVING ROOM").

**Punctuation as ornament.** The **middot ` · `** (space-middot-space) is the
signature separator everywhere: captions, eyebrows, folios
(`The Living Room · Garden Side`, `Plate 01 · Our Process`). Curly quotes only.
Em dashes for asides.

**Numbering.** Pages are *Plates* (`Plate 01`…); process steps carry oversized
Franklin Gothic numerals with a tiny "of seven" style sub-label.

**Examples of real copy:**
- Eyebrow: `An Introduction` / `Plate 01 · Our Process`
- Caption: `The Living Room · Garden Side`
- Headline: *"Every house begins as a conversation."*
- Fee row label: `Schematic Design` → value `15%`; total label is simply `Total`.

**No emoji. Ever.** The system uses no emoji and no decorative Unicode beyond the
middot, curly quotes, and thin rules.

---

## VISUAL FOUNDATIONS

**Color.** A single warm accent — **rust / terracotta `#A2512D`** — does all the
expressive work, sitting on **cream paper `#FBF6EE`**. Text is warm brown ink
(`#2A2520` primary, softening to `#6E5E52` and `#8E7E72`). Dark grounds (footer,
cover) use near-black **night `#1a1714`** with rust-soft and cream type over it.
There are **no blues, no greens, no gradients-as-decoration** — the only
gradients are subtle photographic scrims (transparent → dark) to seat captions.

**Type.** Five families, each with a fixed job:
- **Aviano Sans** (`--display`) — the logo voice; bold uppercase nameplates + labels.
- **Columbia Titling** (`--titling`) — classical inscriptional caps for eyebrows,
  nav, folios, micro-labels. Always uppercase, very wide tracking (.30–.46em).
- **URW Antiqua** (`--serif`) — body copy *and* the big italic headlines. The
  workhorse.
- **Franklin Gothic Condensed / Compressed** (`--sans-cond` / `--sans-comp`) —
  oversized numerals, prices, plate numbers. Provides industrial contrast.

**Spacing & layout.** Generous. Body content is capped at `--page-max: 1180px`
with an 80px gutter (40/24px on smaller screens). The signature content layout is
a two-column grid: a **220px "side" column** (giant numeral + rule + label) beside
a **660px-max text column**. Vertical rhythm is built from large section paddings
(60–96px) separated by hairline rules.

**Borders & rules.** Thin **hairlines** are structural, not decorative —
`rgba(162,81,45,0.32)` rust at 1px sits under captions, between fee rows, above
footers. A stronger 65% rust hairline tops the fee table. The recurring graphic
accent is a **40×2px solid rust bar** (`.cm-rule`).

**Imagery.** Large, warm, naturally-lit architectural photography — full-width
hero blocks with `16/11` (or `16/9`, `4/5`) aspect ratios. On content pages the
hero is a **horizontal scroll-snap slideshow** (rust arrows on hover, cream dots).
Every image carries a single ALL-CAPS caption beneath it in Columbia Titling.
A faint bottom scrim (`transparent 70% → rgba(15,12,10,.12)`) grounds each photo.

**Cards.** Restrained. Cards are flat fills of `--paper-edge` with **no rounding**
(square corners throughout) and **no drop shadows** — separation comes from the
cream tint and hairline borders, not elevation. Hover lightens the fill and adds a
hairline border.

**Corners & shadows.** **Square corners everywhere** — there is no border-radius
in the system. **No box-shadows.** The aesthetic is printed-paper-flat.

**Motion.** Subtle and quick. Transitions run **160–220ms** on color, border,
background, and opacity. Slideshow scrolling uses smooth scroll-snap. No bounce,
no spring, no parallax. The mobile menu and burger animate over 200ms.

**Hover / press states.**
- Links: ink → **rust** on hover; active nav gains a rust bottom-border.
- Buttons/CTA (bordered): fill with rust, text flips to cream.
- Image arrows: cream → rust fill, rust → cream glyph.
- Cards / page-nav: fill lightens to `#f5ecdb`, hairline border appears.
No scale-down press states; interactions are color-driven.

**Transparency & blur.** Used sparingly and purposefully: the sticky nav row is
`rgba(251,246,238,0.92)` with a 12px backdrop-blur; image arrows are translucent
cream with a 4px blur. Photographic scrims use layered black at low alpha.

---

## ICONOGRAPHY

The brand is **almost entirely typographic** — it leans on letterforms, rules,
and numerals rather than icons.

- **Logos.** `assets/logo-wordmark.png` is the primary lockup: "CARLISLE / MOORE /
  ARCHITECTS" stacked in rust Aviano caps, with a distinctive **interlocking "OO"**
  ligature in MOORE. `assets/logo.png` is the same mark with more padding.
- **House mark.** `assets/house.png` — a small, painterly rust house glyph
  (chimney + gable). Used as a quiet secondary mark / favicon-scale accent.
- **Divider.** `assets/divider.png` — a 1500×136 decorative rule strip.
- **No icon font, no SVG icon set.** Navigation arrows are **typographic
  glyphs** (`‹` / `›` set in URW Antiqua), not iconography. The hamburger menu is
  built from three CSS bars.
- **No emoji, no Unicode symbol fonts.** The only repeated glyphs are the middot
  `·`, curly quotes `" "`, and thin CSS rules.

If a future surface genuinely needs UI icons (not present in the current brand),
substitute a thin, classical line set and **flag the substitution** — nothing in
the existing material establishes an icon language.

---

## Using this system

1. `@import` or copy `colors_and_type.css` and use the `--*` tokens — never
   hard-code hexes or font names.
2. Compose with the editorial roles: eyebrow (Titling caps) → italic serif
   headline → serif body, with a numeral/label side column for structure.
3. Keep corners square, drop shadows off, and let hairline rules + the rust
   accent carry the structure.
4. Pull real photography from `assets/photos/` and always caption it in
   uppercase Titling with a middot separator.
5. For full component markup, see `ui_kits/website/`.
