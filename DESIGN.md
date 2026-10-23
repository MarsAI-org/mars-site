---
name: Mars (Reference Sheet)
description: A technical reference sheet printed on uncoated stock, built on man-page grammar.
colors:
  primary: "#bf2f1c"
  primary-hover: "#131110"
  neutral-bg: "#f2efe7"
  neutral-surface: "#faf8f3"
  neutral-ink: "#131110"
  neutral-soft: "#57504a"
  rule: "#c9c3b6"
  rule-hard: "#a9a294"
typography:
  display:
    fontFamily: "Archivo, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(3.5rem, 1.6rem + 7.4vw, 7.5rem)"
    fontWeight: 800
    lineHeight: 0.8
    letterSpacing: "-0.035em"
  heading:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "0.9375rem"
    fontWeight: 700
    lineHeight: 1.6
    letterSpacing: "0.17em"
  lead:
    fontFamily: "Archivo, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(1.1875rem, 1.1rem + 0.5vw, 1.4375rem)"
    fontWeight: 500
    lineHeight: 1.35
    letterSpacing: "-0.015em"
  body:
    fontFamily: "Archivo, Helvetica Neue, Helvetica, Arial, sans-serif"
    fontSize: "clamp(1.0625rem, 1rem + 0.22vw, 1.125rem)"
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: "normal"
  small:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "0.9375rem"
    fontWeight: 500
    lineHeight: 1.5
    letterSpacing: "0.12em"
  code:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "1rem"
    fontWeight: 500
    lineHeight: 1.3
    letterSpacing: "normal"
rounded:
  square: "0"
spacing:
  gutter: "clamp(1.15rem, 4vw, 4.5rem)"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.neutral-bg}"
    rounded: "{rounded.square}"
    padding: "0.7rem 1.15rem"
    height: "2.75rem"
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
    textColor: "{colors.neutral-bg}"
    rounded: "{rounded.square}"
  surface-plate:
    backgroundColor: "{colors.neutral-surface}"
    textColor: "{colors.neutral-ink}"
    rounded: "{rounded.square}"
    padding: "0.85rem 1rem"
---

# Design System: Mars (Reference Sheet)

## Overview

**Creative North Star: "mars(1), Set and Printed".**

Mars is a command-line tool with deep systems roots: language servers, debuggers
over DAP, and an in-process Rust core that replaces external utilities. The page
treats the product as a document that signs its own work — its own man page,
printed on heavy uncoated reference stock with dense carbon ink, red hairline
rules and markers, and a rubber stamp that verifies the issue.

The world is a mid-century technical reference sheet, refusing both the dark
terminal-and-neon look and the equal-card SaaS grid. Sections are organized
strictly under man-page conventions: NAME, SYNOPSIS, DESCRIPTION, PARAMETERS,
FLAGS, FILES, EXAMPLES, and a closing colophon.

**Key Characteristics:**
- A strict section ladder: an all-caps label rail on the left bounded by a 1px vertical rule, with red tick marks anchoring each entry.
- Uncoated reference stock (`#f2efe7`) with a faint procedural grain tile, carbon ink (`#131110`), and rubber-stamp red (`#bf2f1c`) as the only accent.
- One variable typeface, Archivo, width-stepped from compressed 62% display caps to 100% reading roman; monospace is reserved strictly for machine literals.
- Flat surfaces separated by hairlines; no cards, no rounded corners, no soft drop shadows, and no decorative glow.
- Working technical controls: an OS switcher that updates path, privilege and script links together; two-state flag markers; a physical measuring ruler for stages.

## Colors

A print palette of three functional inks and two stock tones.

### Primary
- **Stamp Red** (`#bf2f1c`): the accent. The rubber stamp, the prompt sigil, active markers, the section ticks, and the primary copy action. 5.02:1 on reference stock.

### Neutral
- **Reference Stock** (`#f2efe7`): the uncoated ground across the entire page, overlaid with an imperceptible 180px grain tile.
- **Sheet Plate** (`#faf8f3`): the installer plate, input well, and capture backings.
- **Carbon Ink** (`#131110`): the principal text and boundary ink. 16.39:1 on reference stock.
- **Soft Carbon** (`#57504a`): secondary notes, meta facts, parameter glosses, and colophon text. 6.89:1 on reference stock.
- **Hairline Rule** (`#c9c3b6`): internal horizontal and vertical section dividers.
- **Hard Rule** (`#a9a294`): the title-block divider and bounding rules.

### Named Rules
**The Red Is a Mark Rule.** Stamp red is a mark, a tick, a stamp, or an armed state. It never sets a sentence.

**The No-Shadow Rule.** Depth is created through hairline rules and tone steps between reference stock and sheet plates. Surfaces are flat; no shadows exist.

## Typography

**One variable family: Archivo** (100–900 weight, 62–125% width, self-hosted from `assets/fonts/archivo-var.woff2`). Monospace (`ui-monospace, SFMono-Regular, Menlo, monospace`) is strictly reserved for literal commands, flags, and parameter keys.

### Hierarchy
- **Display** (800, 62% width, `clamp(3.5rem, 1.6rem + 7.4vw, 7.5rem)`, 0.8 line-height): the `mars(1)` title block only.
- **Heading** (700, 100% width, `0.9375rem`, 1.6 line-height, 0.17em tracking): section labels in the ladder, uppercase monospace.
- **Lead** (500, `clamp(1.1875rem, 1.1rem + 0.5vw, 1.4375rem)`, 1.35 line-height): the definition clause and the close sentence.
- **Body** (400, `clamp(1.0625rem, 1rem + 0.22vw, 1.125rem)`, 1.55 line-height): running prose, parameter descriptions, and figure captions.
- **Small** (500, `0.9375rem`, 1.5 line-height, 0.12em tracking): meta facts, plate notes, ruler stops, and colophon.
- **Code** (500, `1rem`, 1.3 line-height): literal commands and shell tokens.

### Named Rules
**The Bold Is Literal Rule.** Monospace bold indicates a literal CLI token (`--model`, `mars`); roman bold indicates document structure or emphasis. They are never swapped.

**The Floor Rule.** Nothing meant to be read drops below 15px (0.9375rem).

## Layout

A centered reference sheet capped at 84rem, with equal gutters (`clamp(1.15rem, 4vw, 4.5rem)`) on both sides.

The layout is structured around the section ladder:
- Desktop: a left rail (`clamp(6.5rem, 13vw, 10.5rem)`) holding the section label, bounded on the right by a 1px carbon ink rule with a red tick, and a flexible body area on the right.
- Mobile (under 48rem): the rail collapses; section labels become horizontal header bars with an underline, and the stamp shifts below the title block.

## Elevation & Depth

Surfaces are flat. Depth is communicated strictly by material contrast:
- Reference Stock (`#f2efe7`) sits behind the entire document.
- Sheet Plates (`#faf8f3`) enclose the installer and figures within crisp 1px or 2px rules.
- Boundaries are drawn by 1px Hairline Rules (`#c9c3b6`) and 3px Carbon Ink bars.

## Shapes

Shapes are strictly rectangular with zero radius (`0px`), echoing the cut of paper sheets and letterpress blocks. The only curved elements on the page are the circular rubber stamp and the pixel logo.

### Named Rules
**The Square Edge Rule.** Buttons, plates, inputs, and tabs have square corners (`border-radius: 0`). The stamp is the only drawn circle.

## Components

### Install plate
A 2px carbon-bordered plate in Sheet Plate (`#faf8f3`). The top bar holds the OS tablist and filename; the body holds the command with a red prompt sigil (`$`, `>`) and the stamp-red `COPY` button. Below, a ruled note details installation path, privilege requirements, and script links.

### Flag Switch
A man-page option row (`--lsp`, `--inprocess`) featuring a square two-state marker (`[■]` armed, `[ ]` cleared) that is a full 44px hit target. Toggling arms the flag and smoothly opens the consequence explanation below it.

### Example Ruler
A range input styled as a mechanical measuring ruler with alternating millimeter-scale tick marks and a sliding stamp-red vernier thumb. Stepping through stops switches the figure capture and descriptive prose.

### Repo Blank
An inline text input styled with a red underline rule inside the closing sentence. Entering a repository path automatically rewrites the command across tabs so that clicking `INSTALL` copies the complete `install && cd 'repo' && mars` pipeline.

## Motion

Motion is minimal and physical, like paper being printed:
- The rubber stamp lands once on entry (`scale: 1.5 → 1`, `rotate: -2deg → -8deg`, 520ms).
- The title block divider rules across the sheet via `clip-path` wipe (620ms).
- Switch consequence lines reveal smoothly via CSS grid transition (`grid-template-rows: 0fr → 1fr`, 220ms).
- All transitions respect `prefers-reduced-motion: reduce`, which disables animations and presents the fully-resolved sheet immediately.

## Do's and Don'ts

### Do
- Preserve the man-page section ladder: `NAME`, `SYNOPSIS`, `DESCRIPTION`, `PARAMETERS`, `FLAGS`, `FILES`, `EXAMPLES`.
- Keep every interactive target at least 44px tall.
- Set machine facts and literal syntax in monospace; set running text in Archivo.
- Use stamp red (`#bf2f1c`) only for the stamp, ticks, sigils, and armed states.
- Pre-compose or bake textures so contrast ratios stay ≥ 5.0:1 everywhere.

### Don't
- Add rounded corners, cards, soft shadows, or glowing outlines.
- Set whole sentences in stamp red.
- Use monospace for narrative prose.
- Let interactive controls fall into `hidden` tabpanels upon click.
- Add marketing eyebrows or decorative section numbers above titles.
