---
name: Mars
description: A coding agent landing page built on one motif, the planet, at every scale.
colors:
  accent: "#ef5f2f"
  accent-hover: "#ff7a4f"
  accent-ink: "#14070a"
  bg: "#0a0710"
  surface: "#17101f"
  surface-2: "#211630"
  ink: "#f2ecf5"
  muted: "#ab9cba"
  ok: "#b6f0bd"
  ok-ink: "#101c12"
typography:
  display:
    fontFamily: "Pilcrow Rounded, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(2.75rem, 1.2rem + 5.4vw, 5.5rem)"
    fontWeight: 700
    lineHeight: 0.96
    letterSpacing: "-0.03em"
  heading:
    fontFamily: "Pilcrow Rounded, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(2rem, 1.3rem + 3.2vw, 4rem)"
    fontWeight: 700
    lineHeight: 0.96
    letterSpacing: "-0.03em"
  lead:
    fontFamily: "Pilcrow Rounded, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(1.25rem, 1.1rem + 0.7vw, 1.625rem)"
    fontWeight: 400
    lineHeight: 1.45
    letterSpacing: "normal"
  body:
    fontFamily: "Pilcrow Rounded, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(1.0625rem, 1rem + 0.25vw, 1.1875rem)"
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: "normal"
  small:
    fontFamily: "Pilcrow Rounded, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(1rem, 0.94rem + 0.18vw, 1.0625rem)"
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: "normal"
  wordmark:
    fontFamily: "Pilcrow Rounded, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.375rem"
    fontWeight: 700
    lineHeight: 1
    letterSpacing: "-0.03em"
  statement:
    fontFamily: "Pilcrow Rounded, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(1.25rem, 2.6vw, 2.1rem)"
    fontWeight: 500
    lineHeight: 1.1
    letterSpacing: "-0.02em"
  display-narrow:
    fontFamily: "Pilcrow Rounded, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(2.4rem, 12.5vw, 2.9rem)"
    fontWeight: 700
    lineHeight: 0.96
    letterSpacing: "-0.045em"
  code:
    fontFamily: "ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: "normal"
rounded:
  plate: "1.35rem"
  pill: "999px"
spacing:
  gutter: "clamp(1rem, 3.2vw, 2.5rem)"
components:
  button-primary:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.accent-ink}"
    rounded: "{rounded.pill}"
    padding: "0.55rem 1.05rem"
    height: "2.75rem"
  button-primary-hover:
    backgroundColor: "{colors.accent-hover}"
    textColor: "{colors.accent-ink}"
    rounded: "{rounded.pill}"
  surface-plate:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.plate}"
    padding: "0.75rem"
  tile:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.plate}"
    padding: "1.2rem"
---

# Design System: Mars

## Overview

**Creative North Star: "The Planet Is the Motif".**

Mars is a planet, so a circle runs the entire page. It appears at three wildly
different scales and never in another shape: a 128vh orb cropped by three
viewport edges behind the hero, the round press of every button and plate, the
circular frame the stage captures sit in, the star dots in the field, and the
knob on every switch. One geometry, committed, is the whole system. Sections are
plain single or two-column layouts precisely so the circle is the only thing with
character.

The world is deep space, given by the user: near-black ground with stars, rust
as the one warm light. It is not a starfield wallpaper with a page on top. The
field is a drawn layer at 50% opacity, it drifts over ninety seconds, and the orb
carries the single photograph the page needs: NASA/JPL-Caltech PIA17947, Mount
Sharp on the Martian horizon, multiplied into the rust and wiped by the ground
tone so bone type clears AA over it.

**Key Characteristics:**
- One motif, the circle, at hero, component, and texture scale. No second shape.
- Rust on near-black, and nothing else: no second hue, no gradient fill, no shadow.
- Soft, fully rounded controls against a hard photographic orb.
- Motion is the page's voice: a clip-wipe entrance, staggered children, a
  scroll-driven drift and lean, a live switch, and a slider that redraws the
  section. Every one has a reduced-motion path that leaves the content complete.

## Colors

Two roles plus one status pair.

### Primary
- **Rust** (`#ef5f2f`): the light. It fills the orb, every primary control, the sigil,
  the slider thumb and the two "on" switch bands. Never body copy.
- **Rust Hover** (`#ff7a4f`): the same light raised, on hover only.

### Neutral
- **Void** (`#0a0710`): the ground, behind everything, including the star layer.
- **Slab** (`#17101f`): plates, tiles, switch rows and the stage frame.
- **Slab Deep** (`#211630`): inset wells inside a plate, the range track.
- **Bone** (`#f2ecf5`): headings, body, and any text on the ground. 17.2:1.
- **Dust** (`#ab9cba`): secondary notes and resting switch sentences. 7.8:1 on
  the ground, 7.3:1 on a slab. It is a real reading colour, not a whisper.

### Status
- **Copied** (`#b6f0bd` on `#101c12`): the copy button's success fill only.
- **Copy failed** (`Bone` on `Slab Deep`): the copy button's failure fill, when
  the clipboard API rejects or is missing.

### Named Rules
**The One Light Rule.** Rust is the only warm colour and the only accent. A second
hue is a different world.

**The Mark, Not the Read Rule.** Rust never sets a sentence. It sets a sigil, a
fill, a dot, a thumb.

## Typography

**One family: Pilcrow Rounded** (400 / 500 / 700, self-hosted from
`assets/fonts/pilcrow-rounded-*.woff2`). Fully rounded stroke ends, bold and tight: the terminals are the motif at letter scale, so the type and the circle are the same gesture. It
carries the headlines, the running text, the figures and the switch sentences.

The monospace stack is only for literal commands inside `<code>`. Pilcrow Rounded
is the voice; monospace is the machine's own output.

### Hierarchy
- **Display** (700, `clamp(2.75rem, 1.2rem + 5.4vw, 5.5rem)`, 0.96, -0.045em):
  the hero only, capped at 15ch, dropping to 12ch and a smaller step below 24rem.
- **Heading** (700, `clamp(2rem, 1.3rem + 3.2vw, 4rem)`, -0.03em, capped at 18ch):
  section headings.
- **Lead** (400, `clamp(1.25rem, 1.1rem + 0.7vw, 1.625rem)`): the hero lede and
  the stage clause.
- **Body** (400, `clamp(1.0625rem, 1rem + 0.25vw, 1.1875rem)`): running text,
  held to 62ch.
- **Small** (400, `clamp(1rem, 0.94rem + 0.18vw, 1.0625rem)`): notes, plate
  meta, stops. Never below 16px, so nothing meant to be read is smaller than body
  by more than one step.

### Component steps
Three sizes exist only on one component each, mapped to the nearest ramp step: the wordmark at 1.375rem, the switch sentence at `clamp(1.25rem, 2.6vw, 2.1rem)`, and the hero headline at `clamp(2.4rem, 12.5vw, 2.9rem)` below 24rem so it holds two lines.

### Named Rules
**The One Family Rule.** No second face, no italic, no serif accent word.
Emphasis is weight and size.

**The Floor Rule.** Nothing meant to be read drops under 16px.

## Layout

One centred shell at 78rem with a gutter of `clamp(1rem, 3.2vw, 2.5rem)`, equal
on both sides at every width. Stacked to two columns at 50rem; the tile board
runs four across, two below 52rem.

The hero is `min(84svh, 46rem)` with copy on the left and the orb anchored at 74%
and cropped on three edges. Below 50rem the orb stays behind the type and the copy
takes the full gutter; the copy holds the lead step there rather than shrinking
to body. The photograph is pre-composited in the file itself (multiplied into the
rust, 0.8 over the disc, veil baked in, 0.9 opacity under 50rem) so contrast does
not depend on a stacking layer; the measured floor is 5.2:1 under the headline.

Section rhythm is 3.5–7rem. The close inverts it: a two-column grid with the
sentence at 24ch on the left and the note aligned to its baseline on the right.

### Named Rules
**The Equal Margin Rule.** Both gutters are the same everywhere. A crop is the
only thing allowed past them.

**The No Empty Half Rule.** Every wide layout closes its far side with the orb,
the picture, the switch, or a second column.

## Elevation & Depth

There are no shadows. Depth is a tone step (Void → Slab → Slab Deep) and the
circle's own scale. Nothing lifts.

## Shapes

The circle is the shape system; radius is `999px` on every interactive control
and `1.35rem` on plates and tiles. The stage frame is a full circle, which crops
each capture to its centre and keeps the four screenshots the same object. The
tile board is the one square corner set, because it is a board.

### Named Rules
**The One Shape Rule.** A circle at hero, control, texture and frame scale. A
square is only the board grid.

## Components

### Install plate
`--slab` plate at 1.35rem, an OS pill well at the top with the file name opposite,
then the command on `--bg` inside a pill with the copy button at its right. The
plate mirrors the chosen OS tab: file name, install path, privilege phrase and the
linked script all swap together. Below, one Dust line states the path, the
privilege and the script link.

The prompt sigil (`$`, `>`) is a `.cmd` child beside the `<code>`, so the
clipboard always receives the bare command. The repo blank in the close appends
its own segment to both commands, quoted, so what is shown is what is copied.

Copy has three states: rest (Rust), copied (`--ok` on `--ok-ink`, 2.4s), and
failed (`--surface-2` on `--ink`). The label swaps with the fill and a `role=
"status"` line below the plate announces the outcome in words, then clears.

### Tiles
A `--slab` slab at 1.35rem holding one provider name, 3:2. The first tile spans
two columns in Rust and carries the section heading instead of a name. No numbers,
no icons.

### Switch row
A full-width `--slab` row, rounded, with the consequence sentence at 1.25–2.1rem
in Dust, and a real `role="switch"` knob at the right. Off, the row is dark. On,
the row floods Rust, the sentence turns `--accent-ink` (5.96:1) and the
consequence line opens beneath it. Two rows start on. Click, Space and Enter all
work; the knob is 44px tall. The open line is capped at 8rem, which clears its
two-line worst case at 320px.

### Stage slider
A real `input[type=range]` with four stops. The thumb is a Rust circle. Moving it
swaps the clause, the stop highlight and the visible capture in a 260ms crossfade.
Nothing depends on scroll position.

### Close sentence
A statement at the display-adjacent step with two real fields inline: a text
input on `--surface-2` for the repo name, and the final word as a Rust button.
Both scale with the sentence in `em` and stay at least 44px tall. The blank
rewrites the command in both OS tabs as it is typed; Enter submits, and the
button switches to the POSIX tab, scrolls the plate into view, focuses its copy
control and copies there, so focus never lands on a hidden panel.

## Motion

The loud moment is the orb: it opens with a `clip-path` wipe while the photograph
inside settles from 1.14 to rest, 1.05s, once. Then:

- the headline wipes in behind it;
- tiles, switch rows and notes arrive on a 60–120ms stagger as they enter;
- the orb drifts against the scroll up to 90px;
- the stage frame leans back 2% while it is off-centre and settles when it centres;
- every control answers hover and press; the knob stretches its thumb on press.

The field drifts over 90s. All of it is transform, opacity, clip-path and
transition, all of it under `prefers-reduced-motion: no-preference`, and the
reduced path removes the drift and the wipe while keeping every element at full
opacity and in place. The hidden entrance states are scoped to `.js`, which the
script adds to `<html>`, so a visitor without scripts sees the finished page
instead of a blank one.

### Named Rules
**The Content-First Rule.** No entrance may hide content that the script has not
already revealed, and reduced motion shows the finished frame.

**The Live-Focus Rule.** An action that moves focus names its destination tab
first; focus never lands on a panel that is `hidden`.

## Do's and Don'ts

### Do
- Keep one motif and one light.
- Round every control fully; round plates at 1.35rem.
- Set machine facts in `<code>` and everything else in Pilcrow Rounded.
- Keep every control at least 44px tall and give it a visible focus ring.
- Add motion with a transform or opacity, and give it a reduced-motion path.
- Keep bone copy at 4.5:1 over the orb; re-bake the veil into the asset when the
  disc moves under the type.
- Put anything that travels to the clipboard in `<code>` alone, never beside a
  decorative sigil.

### Don't
- Add a second shape, a second accent, a gradient fill, or a shadow.
- Set a sentence in rust.
- Set anything meant to be read under 16px.
- Let the orb cover the headline at any width.
- Add decorative numbering or an eyebrow above a heading.
