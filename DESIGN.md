---
name: Mars (Public Register)
description: A civic bureau's prospectus for a released instrument — a disciplined public register on airy late-modern paper, one violet accent, a flowing ribbon.
colors:
  primary: "#685ce7"
  primary-deep: "#4d43cf"
  primary-wash: "#eceafd"
  mint: "#7fd8d0"
  mint-hover: "#9ee6df"
  indigo: "#5b4fd6"
  ground: "#f7f7fa"
  plate: "#ffffff"
  plate-2: "#f2f2f7"
  ink: "#1b1547"
  body: "#4b5165"
  soft: "#6c7186"
  hairline: "#e6e7ee"
  hairline-hard: "#d3d4e0"
  warn: "#b26a14"
  success: "#24804e"
  danger: "#b23b3b"
  on-ink-muted: "#c9c7e6"
typography:
  display:
    fontFamily: "Hanken Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(2.75rem, 1.2rem + 6.6vw, 6rem)"
    fontWeight: 500
    lineHeight: 0.98
    letterSpacing: "-0.03em"
  headline:
    fontFamily: "Hanken Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(1.5rem, 1.1rem + 1.8vw, 2.25rem)"
    fontWeight: 600
    lineHeight: 1.1
    letterSpacing: "-0.02em"
  lead:
    fontFamily: "Hanken Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(1.125rem, 1.05rem + 0.4vw, 1.375rem)"
    fontWeight: 500
    lineHeight: 1.36
    letterSpacing: "normal"
  body:
    fontFamily: "Hanken Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(1rem, 0.96rem + 0.2vw, 1.0938rem)"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "normal"
  label:
    fontFamily: "Spline Sans Mono, ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "0.75rem"
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: "0.16em"
  code:
    fontFamily: "Spline Sans Mono, ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "0.9375rem"
    fontWeight: 500
    lineHeight: 1.3
    letterSpacing: "normal"
rounded:
  control: "8px"
  chip: "4px"
  micro: "2px"
  plate: "14px"
spacing:
  gutter: "clamp(1.25rem, 4.5vw, 3.75rem)"
  section: "clamp(2.5rem, 6vw, 5rem)"
  shell: "78rem"
components:
  button-primary:
    backgroundColor: "{colors.primary-deep}"
    textColor: "{colors.plate}"
    rounded: "{rounded.control}"
    padding: "0 1.05rem"
    height: "2.75rem"
  button-primary-hover:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.plate}"
    rounded: "{rounded.control}"
  button-mint:
    backgroundColor: "{colors.mint}"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "0 0.6em"
  chip-token:
    backgroundColor: "{colors.primary-wash}"
    textColor: "{colors.primary-deep}"
    rounded: "{rounded.chip}"
  chip-filter:
    backgroundColor: "{colors.plate}"
    textColor: "{colors.body}"
    rounded: "{rounded.control}"
    height: "2.25rem"
  chip-filter-pressed:
    backgroundColor: "{colors.primary-deep}"
    textColor: "{colors.plate}"
    rounded: "{rounded.control}"
  input-blank:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.mint}"
    rounded: "{rounded.control}"
  plate:
    backgroundColor: "{colors.plate}"
    textColor: "{colors.ink}"
    rounded: "{rounded.plate}"
    padding: "1.4rem 1.4rem 1.5rem"
---

# Design System: Mars (Public Register)

## Overview

**Creative North Star: "Public intent, measurable progress."**

Mars is a serious native instrument, and this page is the register it keeps for
itself: a civic bureau's prospectus, printed on airy late-modern paper. It refuses
both the dark terminal-and-neon hero that every coding tool ships and the
equal-card SaaS grid. Instead the ledger *is* the argument — every capability is
one attributed entry with a state and a piece of evidence attached, and the
install command is the register's own closing action.

The world is light, disciplined and calm, but not beige: a cool near-white ground,
deep navy-violet ink, and a single committed violet accent, with one flowing
mint→violet→indigo ribbon as the page's only gesture. Material is paper and
engraving — crisp white plates on hairline keylines, a soft single shadow, a
halftone city silhouette, mono literals for anything the machine reads.

**Key Characteristics:**
- Cool paper ground (`#f7f7fa`) with white plates and hairline keylines; no cream, no glass.
- One committed accent — violet (`#685ce7`) — carried by state signs, tokens, links and the action, never by whole sentences.
- A register grammar: sections are citizen-facing titles with a left-aligned body and a mono meta column; entries are signed (`+` / `~` / `−`) and dated by release line.
- Hanken Grotesk for the voice (display 500, reading 400); Spline Sans Mono only for machine literals — versions, refs, commands, paths.
- One ribbon gradient, one halftone skyline; depth from a soft single elevation, never glow.

## Colors

A cool page of three inks and two grounds, with one committed accent.

### Primary
- **Register Violet** (`#685ce7`): the accent and the fill. Large display clauses, the ribbon's mid-stop, dots, active nav and the install action's deeper tone. 4.6:1 on ground for large text.
- **Register Violet Deep** (`#4d43cf`): the working tone for small accent text — links, token chips, unit labels, section signs, the Copy and Get buttons. 6.5:1 on ground; use it wherever violet must set readable small type.
- **Violet Wash** (`#eceafd`): the flat tint behind token chips and selected tabs.

### Secondary
- **Halftone Mint** (`#7fd8d0`): the ribbon's light stop and the close plate's action ink. Never on the light ground.

### Tertiary
- **Ribbon Indigo** (`#5b4fd6`): the ribbon's deep stop and the halftone skyline's dot ink.

### Neutral
- **Cool Paper** (`#f7f7fa`): the page ground everywhere.
- **Register Plate** (`#ffffff`): the install plate, instrument row, and exhibits' frames.
- **Well Plate** (`#f2f2f7`): the command well and default switch fills.
- **Carbon Ink** (`#1b1547`): principal text, the close plate, the table rules' emphasis. 15.8:1 on ground.
- **Draft Body** (`#4b5165`): running prose and secondary copy. 7.4:1 on ground.
- **Draft Soft** (`#6c7186`): meta facts, mono labels, colophon notes. 4.5:1 on ground; never for body.
- **Keyline** (`#e6e7ee`): internal dividers. **Keyline Hard** (`#d3d4e0`): plate and section boundaries.
- **Docket Amber** (`#b26a14`): the `~` fixed sign only.
- **Copy Success** (`#24804e`): the Copy button's confirmed state only. **Copy Failure** (`#b23b3b`): its failed state only.
- **Muted on Ink** (`#c9c7e6`): the close plate's placeholder and secondary text on the dark field.

### Named Rules
**The One Accent Rule.** Violet is the only chromatic accent on the light ground. Everything else is ink, body, or keyline. Its scarcity is what makes the state signs read.

**The Small Text Deepens Rule.** Small violet text (below ~18px) uses Register Violet Deep (`#4d43cf`), never Register Violet (`#685ce7`). The brighter violet is for fills and large display only, where it clears contrast on size.

## Typography

**Display & Body Font:** Hanken Grotesk (with Helvetica Neue, Helvetica, Arial)
**Label & Mono Font:** Spline Sans Mono (with ui-monospace, SFMono-Regular, Menlo)

**Character:** A humane late-modern grotesque with a high x-height and gently
rounded terminals — precise enough to read as a government register, warm enough
not to feel like a system default. The mono is a humanist companion for machine
literals; it never sets a sentence.

### Hierarchy
- **Display** (500, `clamp(2.75rem, 1.2rem + 6.6vw, 6rem)`, 0.98 line-height, -0.03em): the prospectus headline only.
- **Headline** (600, `clamp(1.5rem, 1.1rem + 1.8vw, 2.25rem)`, 1.1, -0.02em): section titles and the close sentence.
- **Lead** (500, `clamp(1.125rem, 1.05rem + 0.4vw, 1.375rem)`, 1.36): the hero lede, entry text, flag text.
- **Body** (400, `clamp(1rem, 0.96rem + 0.2vw, 1.0938rem)`, 1.6): running prose, evidence notes, measured to 46–68ch.
- **Label** (600, `0.75rem`, 0.16em tracking, uppercase): mono meta — section labels, rail titles, tags, colophon.

### Named Rules
**The Literal Is Mono Rule.** Monospace is reserved for what the machine reads or writes: version refs, flags, commands, paths, counts. Narrative prose is always Hanken.

**The No-Eyebrow Rule.** A section title carries its own weight; there is no small label above a heading to introduce it.

## Layout

A centered register capped at 78rem, gutters `clamp(1.25rem, 4.5vw, 3.75rem)`.
Sections are separated by a single hairline and `clamp(2.5rem, 6vw, 5rem)` of
vertical air, with more space above a title than below it.

The hero is an asymmetric two-column prospectus: the headline block on the left,
the live install plate on the right, the halftone skyline and ribbon flowing
under it. The register section is a two-column ledger — a sticky left rail
(15rem) holding release lines and the target matrix, and the signed entries on
the right. Under 62rem the hero and the register collapse to one column and the
rail un-sticks; the instrument row goes two-up, then one-up under 30rem; the
provider index steps four → three → two → one columns.

## Elevation & Depth

A hybrid: paper depth by tonal steps and keylines, with a light elevation reserved
for real plates. The ground, the well plate and the white plate are three flat
tones separated by hairlines; the install plate, instrument row and exhibits sit
slightly above on a soft, neutral, single shadow. There is no glow, no colored
halo, and no shadow on flat content.

### Shadow Vocabulary
- **plate** (`0 1px 2px rgba(18,16,34,0.05), 0 12px 32px -18px rgba(18,16,34,0.22)`): the default elevation for install plate, instrument row, exhibits, chips' thumbs.
- **lift** (`0 2px 4px rgba(18,16,34,0.06), 0 24px 60px -28px rgba(18,16,34,0.32)`): the hero install plate, standing above the fold.

### Named Rules
**The Neutral Elevation Rule.** Every shadow is neutral near-black, offset, and softly blurred. Shadows never carry the accent color.

## Shapes

Rectangular but softened: controls and chips use an 8px radius, plates and the
close panel a 14px radius, inline chips and the repo blank a 4px radius, and
micro marks (dots, fact bullets) 2px. The only round forms are status dots, the
switch's indicator, and the ruler thumb. Borders are 1px hairlines or 1px
keyline-hard; the close panel is a solid ink field with no border.

### Named Rules
**The Soft-Corner Rule.** Controls are 8px, plates are 14px, and nothing is a pill. The register is precise, not playful.

## Components

### Buttons
- **Shape:** 8px radius (`var(--radius)`), 2.75rem minimum height.
- **Primary (Copy / Get):** Register Violet Deep fill (`#4d43cf`), white label in uppercase mono, padding `0 1.05rem`. Hover darkens to Carbon Ink.
- **Mint action (close):** Halftone Mint fill, Carbon Ink label, sits inline inside the close sentence as a clickable word.
- **Ghost (nav):** text-only nav links in Draft Body, deepening to violet on hover.

### Chips
- **Token chip:** Violet Wash fill, Register Violet Deep mono text at 0.86em, 4px radius. Marks a literal — a flag, a subsystem name, an inline token.
- **Filter chip:** a plate pill in mono uppercase with a tabular count. Pressed state fills with Register Violet Deep and white label; hover deepens the border to violet. The row reports the register's own totals (`all / added / removed`).

### Register Controls & Interaction
The register is interactive, not a poster: it filters, searches, deep-links and
keys.
- **Filter + search:** the chip row narrows the ledger by state, and the search
  field narrows it by text; an empty state replaces the ledger when nothing
  matches. While any filter is on, the version rail dims every release line that
  no longer carries a visible entry and lights the ones that do.
- **Deep links:** `#entry-N` opens that entry and flares its background once;
  `#install-windows` / `#install-macos` select the install tab. Each entry carries
  a `Link` control that writes its permalink to the URL and the clipboard.
- **Keyboard:** `/` focuses the filter; `↑` / `↓` step the visible entries; `Esc`
  clears the filter and query.
- **Motion:** counts tick up once on entry, evidence reveals on a grid-row
  transition, a hovered entry row washes and nudges its sign. Every gesture is
  suppressed under `prefers-reduced-motion`.

### Plates / Containers
- **Corner Style:** 8px for the install plate's controls, 14px for full plates.
- **Background:** Register Plate (`#ffffff`) or Well Plate (`#f2f2f7`) for the command well.
- **Border:** 1px Keyline Hard for the outer edge, 1px Keyline for internal rules.
- **Shadow:** the plate elevation; nothing else.
- **Padding:** `1.4rem` on instrument cells; `0.85rem` on the command row.

### Inputs / Fields
- **Style:** the repo blank is an inline underline field inside the close sentence — transparent, mint bottom border, mint mono text, 4px top radius.
- **Focus:** widens to 16ch and keeps a mint focus ring.

### Navigation
- **Style:** a text nav in the masthead, Draft Body, right-aligned before the square Get button. Hover deepens to violet. Collapses to wrapped rows on small screens.
- **Register line:** below the masthead, a mono hairline strip of instrument facts (licence, targets, core) with violet values.

### Signature: The Signed Entry
The register's ledger row: a large `+` / `~` / `−` state sign in the accent, the
capability as one lead-size line with inline mono token chips, a right-aligned
mono version-and-state column, and an action line pairing an `Evidence` toggle
with a `Link` permalink. `Evidence` opens a grid-row reveal holding a short note
plus a dark terminal exhibit; `Link` copies the entry's deep link. Each entry is
one line of truth with a state, its proof and its address — the page's core
device.

## Do's and Don'ts

### Do:
- **Do** keep the section ladder in citizen-facing titles and put meta in the mono label voice.
- **Do** set machine literals — versions, flags, commands, paths, counts — in Spline Sans Mono, and narrative in Hanken Grotesk.
- **Do** carry state with the signed-entry device: a colored sign, a version, a state word, an openable exhibit.
- **Do** keep violet as a mark — state, token, link, action — and deepen it (`#4d43cf`) for small text.
- **Do** give every interactive target a 44px (2.75rem) minimum height and a visible focus ring.
- **Do** make the register addressable and reachable: deep-link each entry and each install tab, and keep `/`, arrow keys and `Esc` working.

### Don't:
- **Don't** add an eyebrow or kicker label above a heading.
- **Don't** set whole sentences in violet, and don't use violet for body copy.
- **Don't** use cream, glass, blur, glow, or a colored halo; elevation is neutral and soft.
- **Don't** use monospace as a costume for "technical" — only for things the machine reads.
- **Don't** rebuild the register as equal cards of icon-plus-heading-plus-text; the signed entry is the unit.
