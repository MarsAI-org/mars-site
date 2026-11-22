---
name: Mars (Editorial Instrument)
description: A crisp light editorial instrument sheet anchored directly to the Mars pixel-art logo — warm alabaster ground, pure white plates, deep obsidian ink, and Mars terracotta orange as the sole chromatic accent.
colors:
  primary: "#d64a27"
  primary-deep: "#b43618"
  primary-crater: "#9b3220"
  primary-wash: "#fdf0eb"
  primary-border: "#efc6b7"
  ember: "#ff825c"
  ember-hover: "#ffa082"
  ground: "#faf8f5"
  plate: "#ffffff"
  plate-2: "#f2eee8"
  plate-3: "#eae4dc"
  ink: "#161419"
  body: "#4a4440"
  soft: "#6b625c"
  hairline: "#e8e2d9"
  hairline-hard: "#d4cbc0"
  obsidian: "#161419"
  obsidian-2: "#211e26"
  on-dark: "#f5f2ee"
  on-dark-muted: "#c2bab2"
  success: "#1f7a4c"
  warn: "#9a580e"
  danger: "#b83227"
typography:
  display:
    fontFamily: "Hanken Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(2.65rem, 1.25rem + 5.6vw, 5.15rem)"
    fontWeight: 600
    lineHeight: 0.96
    letterSpacing: "-0.036em"
  headline:
    fontFamily: "Hanken Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(1.6rem, 1.15rem + 1.8vw, 2.35rem)"
    fontWeight: 600
    lineHeight: 1.08
    letterSpacing: "-0.025em"
  lead:
    fontFamily: "Hanken Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(1.125rem, 1.05rem + 0.36vw, 1.3125rem)"
    fontWeight: 500
    lineHeight: 1.46
    letterSpacing: "normal"
  body:
    fontFamily: "Hanken Grotesk, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(1rem, 0.96rem + 0.18vw, 1.0625rem)"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "normal"
  label:
    fontFamily: "Spline Sans Mono, ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "0.75rem"
    fontWeight: 600
    lineHeight: 1.5
    letterSpacing: "0.08em"
  code:
    fontFamily: "Spline Sans Mono, ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "0.9375rem"
    fontWeight: 500
    lineHeight: 1.35
    letterSpacing: "normal"
rounded:
  chip: "4px"
  control: "8px"
  plate: "14px"
spacing:
  gutter: "clamp(1.25rem, 4.2vw, 3.5rem)"
  section: "clamp(2.75rem, 6.2vw, 5.25rem)"
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
  button-ember:
    backgroundColor: "{colors.ember}"
    textColor: "{colors.obsidian}"
    rounded: "{rounded.control}"
    padding: "0.05em 0.62em"
  chip-token:
    backgroundColor: "{colors.primary-wash}"
    textColor: "{colors.primary-deep}"
    rounded: "{rounded.chip}"
  chip-filter:
    backgroundColor: "{colors.plate}"
    textColor: "{colors.body}"
    rounded: "{rounded.control}"
    height: "2.75rem"
  chip-filter-pressed:
    backgroundColor: "{colors.primary-deep}"
    textColor: "{colors.plate}"
    rounded: "{rounded.control}"
  plate:
    backgroundColor: "{colors.plate}"
    textColor: "{colors.ink}"
    rounded: "{rounded.plate}"
    padding: "1.55rem 1.5rem 1.65rem"
---

# Design System: Mars (Editorial Instrument)

## Overview

**Creative North Star: "Precision hardware sheet, wired straight into the brand."**

Mars is a native coding agent CLI with an in-process Rust core, real language servers, and a real debugger. Its site is a disciplined light editorial specification sheet built directly from the colors of the pixel-art Mars mark (`#d64a27`, `#9b3220`, `#161419`) — warm gallery alabaster ground, pure white elevated plates, obsidian ink, hairline architectural rules, and a single Mars terracotta accent.

It avoids both generic dark-neon developer templates and mismatched decorative palettes. Every section proves the mechanism: a 5-method one-command install workbench above the fold, real zoomable TUI captures, a searchable capability ledger, live CLI flag composition, and honest counts taken directly from the repository.

## Colors

### Primary (Logo-Derived Terracotta)
- **Mars Orange** (`#d64a27`): exact planet body from `mars-mark.svg`. Used for display emphasis, active borders, orbital contour dashes, state signs, and section glyphs.
- **Mars Deep** (`#b43618`): working high-contrast accent for all small text, links, token chips, active tab text, and primary action buttons (`5.9:1` on `#faf8f5`, `6.3:1` on `#ffffff`).
- **Mars Crater** (`#9b3220`): exact crater shade from `mars-mark.svg`. Used for link hover states and secondary orbital markers.
- **Mars Wash** (`#fdf0eb`) & **Mars Border** (`#efc6b7`): light tint and hairline border behind token chips, active walkthrough rows, and active flag switches.

### Neutrals & Dark Surfaces
- **Gallery Ground** (`#faf8f5`): warm, bright editorial page ground.
- **Plate** (`#ffffff`): install workbench, metric row, provider index, and caption footers.
- **Well** (`#f2eee8`): command wells, inactive switch controls, and hover washes.
- **Obsidian Ink** (`#161419`): exact dark ink from `mars-mark.svg`, principal text (`17.5:1` on ground), terminal bezels, lightbox, and closing colophon card.
- **Body Charcoal** (`#4a4440`): running prose (`9.1:1` on ground).
- **Stone Meta** (`#6b625c`): mono labels and metadata (`5.6:1` on ground — clears WCAG AA at small sizes).
- **Hairline** (`#e8e2d9`) & **Hairline Hard** (`#d4cbc0`): crisp internal and outer structural dividers.
- **Ember Coral** (`#ff825c`) & **Ember Hover** (`#ffa082`): accessible high-contrast Mars accent on `#161419` dark surfaces (`8.2:1`).
- **Semantic States**: Success `#1f7a4c`, Warning `#9a580e`, Danger `#b83227`.

### Named Rules
- **The Logo-Rooted Accent Rule.** Mars terracotta/oxide is the sole chromatic accent on light surfaces; never introduce competing purple/cyan/blue accents.
- **The Small Text Deepens Rule.** Any accent text below ~18px uses Mars Deep (`#b43618`), never brighter `#d64a27`, to guarantee WCAG AA contrast (`>= 4.5:1`).
- **The Pixel-Sharp Mark Rule.** Render `assets/mars-mark.svg` with `image-rendering: pixelated` so the pixel-art planet stays razor crisp.

## Typography

- **Display & Reading (`--sans`):** `Hanken Grotesk` (self-hosted WOFF2, weights 400–800). Tight negative tracking on display (`-0.036em`) and headlines (`-0.025em`).
- **Machine Literals (`--mono`):** `Spline Sans Mono` (self-hosted WOFF2, weights 300–700). Reserved strictly for commands, paths, flags, counts, subsystems, and URLs — never long prose.

## Layout & Components

- **Sticky Masthead + Spec Ribbon:** Clean navigation with high-contrast `Install` CTA and a hairline architectural spec bar directly beneath.
- **Hero + 5-Method Install Workbench:** Two-column editorial prospectus paired with a tabbed install plate covering `macOS & Linux`, `Windows`, `Bun`, `Nix`, and `mise` with platform auto-detection, deep links (`#install-posix`, `#install-windows`, `#install-bun`, `#install-nix`, `#install-mise`), SHA-256 verification metadata, and clipboard feedback.
- **4-Stage TUI Walkthrough + Lightbox:** Interactive stage list, synchronized range ruler, dark obsidian terminal bezel, and native `<dialog>` zoom lightbox for full-resolution inspection of real captures (`proof-task`, `proof-lspv`, `proof-review`, `proof-python`).
- **Capability Ledger:** Filter chips (`All / Built-in / Eliminated`), `/` keyboard search, `↑`/`↓` entry navigation, `Esc` reset, sticky subsystem rail, expandable grid-row evidence exhibits, and copyable `#entry-N` permalinks.
- **Live CLI Flags:** Toggle switches (`--prewalk`, `--plan-yolo`, `--advisor`, `--no-lsp`, `--auto-approve`) that compose a live `$ mars ...` preview bar and reveal exact flag semantics.
- **Obsidian Closing Plate:** Dark `#161419` colophon card with a top Mars gradient rule, interactive repo-path input that appends `cd <repo> && mars` safely (POSIX/PowerShell quoted), and visible upstream credits (`oh-my-pi`, `Pi`, MIT).

## Accessibility & Motion

- Minimum `2.75rem` (44px) interactive touch targets, visible `:focus-visible` outlines (`#b43618`), semantic landmarks, ARIA `tablist`/`tabpanel`/`switch`/`status`, and complete `prefers-reduced-motion: reduce` fallbacks.
