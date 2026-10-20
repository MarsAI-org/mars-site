---
name: Mars
description: A coding agent landing page that plays as a surface traverse across a pixel planet.
colors:
  rust: "#d64a27"
  rust-hi: "#ff8a5f"
  focus: "#93d9e3"
  on-rust: "#150609"
  ink: "#0a090d"
  ink-2: "#100e14"
  ink-3: "#16131b"
  ink-4: "#1d1922"
  line: "#2b2532"
  line-2: "#3b3344"
  bone: "#f4ece2"
  dust: "#ada4ad"
typography:
  display:
    fontFamily: "Anybody, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(2.5rem, 1.3rem + 4.6vw, 5rem)"
    fontWeight: 850
    lineHeight: 0.92
    letterSpacing: "-0.035em"
  headline:
    fontFamily: "Anybody, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(1.9rem, 1.4rem + 2.3vw, 3.15rem)"
    fontWeight: 800
    lineHeight: 1.02
    letterSpacing: "-0.028em"
  title:
    fontFamily: "Anybody, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 700
    lineHeight: 1.02
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Anybody, ui-sans-serif, system-ui, sans-serif"
    fontSize: "clamp(1rem, 0.95rem + 0.22vw, 1.0938rem)"
    fontWeight: 400
    lineHeight: 1.62
    letterSpacing: "normal"
  label:
    fontFamily: "Silkscreen, ui-monospace, monospace"
    fontSize: "0.6875rem"
    fontWeight: 400
    lineHeight: 1.62
    letterSpacing: "0.08em"
  metric:
    fontFamily: "Silkscreen, ui-monospace, monospace"
    fontSize: "clamp(1.15rem, 2vw, 1.6rem)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: "0.02em"
  code:
    fontFamily: "ui-monospace, SFMono-Regular, \"SF Mono\", Menlo, Consolas, monospace"
    fontSize: "0.8125rem"
    fontWeight: 400
    lineHeight: 1.62
    letterSpacing: "normal"
rounded:
  none: "0px"
spacing:
  gutter: "clamp(1.25rem, 4vw, 2.5rem)"
components:
  button-primary:
    backgroundColor: "{colors.rust}"
    textColor: "{colors.on-rust}"
    rounded: "{rounded.none}"
    padding: "0.7rem 1.1rem"
  button-primary-hover:
    backgroundColor: "{colors.rust-hi}"
    textColor: "{colors.on-rust}"
    rounded: "{rounded.none}"
    padding: "0.7rem 1.1rem"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.bone}"
    rounded: "{rounded.none}"
    padding: "0.7rem 1.1rem"
  button-secondary-hover:
    backgroundColor: "{colors.ink-3}"
    textColor: "{colors.bone}"
    rounded: "{rounded.none}"
    padding: "0.7rem 1.1rem"
  nav-cta:
    backgroundColor: "{colors.rust}"
    textColor: "{colors.on-rust}"
    rounded: "{rounded.none}"
    padding: "0.5rem 1rem"
    height: "2.75rem"
  chip-tool:
    backgroundColor: "{colors.ink-3}"
    textColor: "{colors.bone}"
    rounded: "{rounded.none}"
    padding: "0.22rem 0.5rem"
  card-surface:
    backgroundColor: "{colors.ink-2}"
    textColor: "{colors.bone}"
    rounded: "{rounded.none}"
    padding: "1.25rem"
---

# Design System: Mars

## Overview

**Creative North Star: "The Surface Traverse"**

The page is a planet you land on and a series of stages you clear. A pixel-art mascot stands on a stepped ridge; each capability is a numbered stage on a rail below the horizon. The interface is built from the same blocks the mascot is built from: flat plates, hard edges, and a 1px seam between every surface. Nothing floats. Nothing glows. Depth comes from the ground ladder — four near-black steps — and from the seam, not from shadow.

The palette is almost entirely absence: near-black grounds, bone type, dust secondary, and one rust accent that behaves like a light source without ever becoming one. Rust marks action and position — the primary plate, the active stage flag, the underline under the current stop, the small square before each meta fact, the stage numerals. It is never used as body text. A single cool cyan exists for one job only: the focus ring.

Two type voices carry the whole system. Anybody, a variable face run wide (108–118% width) and heavy (800–850) for headlines, speaks as the product. Silkscreen, a bitmap face, prints as the machine: stage numerals, OS tabs, commands, labels, spec figures, meta facts. The division is strict — if a human wrote the sentence, it is Anybody; if a machine would print it, it is Silkscreen or monospace.

**Key Characteristics:**
- Flat, bordered plates on a four-step near-black ground ladder; no shadow, blur, or glass anywhere.
- Square corners on every surface; even the mascot and the ridge are built from rectangles and right angles.
- One rust accent, used as fill, flag, dot, and numeral — never as body text.
- Stepped, hard-edged motion: clip wipes in `steps()` frames, not eased fades.
- Body copy held to 62ch; headlines capped at 16–22ch so they break in short, blunt lines.

## Colors

A near-black ground with a single rust light and one cool note held in reserve.

### Primary
- **Mars Rust** (#d64a27): the world's only warm accent. Fills the primary button and the HUD install plate, marks the active stage on the trail rail (2px underline plus a pennant flag), lights the current segment of the HUD stage bar, and sets the 4px square before each meta fact. On dark ground it reads at 4.60:1 — enough for a numeral or a dot, not enough for a paragraph, which is why it never carries body copy.
- **Rust Glow** (#ff8a5f): the lit state of the same accent. Primary button hover fill, inline links, `<em>` emphasis inside the hero headline, stage numerals, and the `$` sigil in a command row. It is a tint of Mars Rust, not a second accent.

### Tertiary
- **Focus Cyan** (#93d9e3): reserved for `:focus-visible` outlines (2px, 3px offset). It appears in no other context in the build.

### Neutral
- **Ground Ink** (#0a090d): page ground, HUD bar, install card bodies.
- **Panel Ink** (#100e14): raised plates — the installer, capture frames, the trail rail, the install band.
- **Bar Ink** (#16131b): inset head bars, hover fills on secondary controls, tool tags.
- **Plate Ink** (#1d1922): the selected OS tab and the copy plate — the top step of the ladder.
- **Seam** (#2b2532): the 1px divider between every surface.
- **Seam Strong** (#3b3344): the outer border of a plate that must read as a separate object, and the inactive segment of the HUD stage bar.
- **Bone** (#f4ece2): primary type, headings, command text.
- **Dust** (#ada4ad): secondary type, ledes, labels, spec keys. Reads 7.16:1 or better on every ground in the ladder.
- **On Rust** (#150609): the near-black that sits on a rust plate. Not declared as a custom property; it is the literal repeated on every rust surface, and it is the contrast-critical half of the primary button (4.58:1).

### Named Rules
**The Rust Is a Verb Rule.** Rust appears as a fill, a flag, a dot, an underline, or a numeral — never as the color of a sentence. The stylesheet has no `color: var(--mars)`; every rust-colored word is Rust Glow.

**The One Cool Note Rule.** Cyan is the focus ring and nothing else. It never becomes a link color, a hover state, a chart accent, or a decorative highlight.

**The Ground Ladder Rule.** Depth steps one rung at a time: Ground Ink → Panel Ink → Bar Ink → Plate Ink. Never skip a rung, never invent a fifth near-black, never lighten a panel to make it "pop" — the 1px seam does that job.

## Typography

**Display Font:** Anybody (variable, 400–900 weight, 75–125% width; self-hosted `assets/fonts/anybody-latin.woff2`)
**Body Font:** Anybody (same file)
**Label/Mono Font:** Silkscreen 400/700 for the machine voice; `ui-monospace` stack for commands, inline code, and tool tags

**Character:** A wide, heavy grotesque against a bitmap face. Anybody carries conviction — headlines run at 850 weight and 118% width, so they look pressed rather than typeset. Silkscreen carries data: it is small, letterspaced, and uppercase, and it is only ever used where a machine would print the words. The pairing reads as a poster printed on a terminal.

### Hierarchy
- **Display** (850, `clamp(2.5rem, 1.3rem + 4.6vw, 5rem)`, 0.92, -0.035em, width 118%): the hero headline only, capped at 16–18ch, stepping down to `clamp(2.25rem, 11.5vw, 3rem)` below 30rem. Emphasis inside it is a color change to Rust Glow, not an italic — `em` is reset to `font-style: normal`.
- **Headline** (800, `clamp(1.9rem, 1.4rem + 2.3vw, 3.15rem)`, 1.02, -0.028em, width 112%): section headings, capped at 22ch. The closing headline uses the display size at 116% width instead.
- **Title** (700, 1.0625rem, 1.02, -0.01em): install card headings, paired with a 1rem stroke icon in Rust Glow.
- **Body** (400, `clamp(1rem, 0.95rem + 0.22vw, 1.0938rem)`, 1.62): running text, held to 62ch; the hero lede is narrower at 46ch and 1.5 line-height.
- **Label** (400, 0.6875rem, 0.08em, uppercase): Silkscreen micro-type — OS tabs, meta facts, trail numerals, alt-install headings, HUD track label.
- **Metric** (400, `clamp(1.15rem, 2vw, 1.6rem)`, 0.02em, tabular figures): spec-sheet values. The unit that follows is set in Anybody at 0.8125rem so the number stays the loud element.
- **Code** (400, `ui-monospace` stack, 0.8125rem, normal tracking): the install commands, inline code, and tool tags. The system stack is deliberate — a downloaded command must look like the reader's own terminal, not like a display face. The installer command steps down to 0.75rem below 34rem so the longest POSIX URL still holds one line.

### Named Rules
**The Two Voices Rule.** Anybody speaks; Silkscreen prints. A sentence a human wrote is never set in Silkscreen, and a machine fact (a numeral, a command, an OS name, a file name) is never set in Anybody.

**The Width Is the Emphasis Rule.** Scale and width move together. Display is 850 weight at 118% width; headline is 800 at 112%; body is 400 at normal width. There is no italic anywhere in the system, and no weight below 400.

**The Measure Rule.** Prose stops at 62ch, the hero lede at 46ch, headlines at 16–22ch. Nothing on the page runs full-width as text.

## Layout

A single centered column on a 74rem shell, with 1px horizontal rules marking every stage boundary. The shell gutter is 1.25rem, widening to 2rem at 40rem and 2.5rem at 75rem. The same gutter value also exists as `--gutter: clamp(1.25rem, 4vw, 2.5rem)` and is used directly by the HUD, the trail rail, and the mascot's left anchor.

Vertical rhythm is section-scale, not component-scale: a stage pads 4.5rem top and bottom, 6.5rem from 48rem, 8rem from 75rem. The proof strip is tighter (3rem → 4rem → 5rem), the closing block is larger (4rem → 5.5rem → 7rem). Within a plate, spacing is set per component in rem — 0.35rem, 0.55rem, 0.85rem, 1.1rem all appear — rather than from a single spacing scale. Spacing does not sit on a 4px grid: the 4px and 6px decorative squares are literals, and `--pixel`, `--edge`, `--step-2`, `--step-5`, `--mars-deep`, and `--cyan` are declared in `:root` but never referenced by a rule.

At 64rem the hero takes `min-height: min(84svh, 46rem)`, the copy column caps at 46rem, and the mascot moves from the left gutter to 10% from the right so its feet still meet the ridge line. Below 63.9375rem the stage reserves the mascot's width as bottom padding so copy never runs under it. Two-column splits engage at 58rem (with a reversed variant that swaps reading order), the three-up proof grid at 52rem, the install pair at 52rem, and the alternative install cards step 1 → 2 → 3 columns at 60rem and 75rem.

Breakpoints present in the build, in rem: 30, 34, 40, 48, 52, 56, 58, 60, 63.9375, 64, 75. They are one-off decisions per component rather than a named scale — 56rem exists to reveal the HUD section links, 63.9375rem is the complement of 64rem for the mascot lane, 60rem is set by the longest install command fitting on one line.

## Elevation & Depth

The system is flat, and this is verified rather than assumed: the stylesheet contains no `box-shadow`, no `text-shadow`, no `drop-shadow`, no `filter`, and no `backdrop-filter`. Depth is conveyed two ways. First, the ground ladder — four near-black steps assigned by layer, so a plate reads as sitting above the page because it is one rung lighter. Second, the seam — a 1px `--line` border between adjacent surfaces, and a 1px `--line-2` outer border when a plate must detach as an object (the installer, a capture frame, the spec sheet's top rule).

There is no shadow vocabulary, so there is no shadow token. Light in this world is a hairline, not a halo: the horizon line above the ridge is a 1px rust gradient that fades to transparent at both ends, and the star field is a fixed layer of 1px radial dots at 28–55% bone opacity. Both are painted behind content and never sit on a surface.

### Named Rules
**The Edge, Not the Lift Rule.** State is signalled by swapping fill or color — never by raising, blurring, or glowing an element. A hover changes background and text color; it does not add a shadow, a translate, or a scale.

**The Seam Rule.** Two surfaces touch through a 1px line, never through a gap, a shadow, or a radius. Adjacent cards are separated by a 1px grid gap filled with `--line`, so the seam is the gap.

## Shapes

Every corner is square. There is no `border-radius` anywhere in the stylesheet, and `rounded: none` is the whole shape system.

The form language comes from the pixel grid, not from geometry: the mascot and brand mark are rendered with `image-rendering: pixelated`, the ridge is an SVG stepped profile sampled on a 48-unit grid, meta facts and capture captions are marked with 4px and 6px solid squares, and the HUD stage bar is a row of 1.25rem × 0.375rem blocks with 3px gaps. Borders are 1px at rest. 2px is reserved for state lines — the focus outline, the active stage underline on the trail, and the underline that thickens on link hover — not for panel edges.

Two silhouettes break the rectangle: the stage flag, a 0.75rem pennant cut with `clip-path: polygon(0 0, 100% 0, 100% 70%, 50% 100%, 0 70%)`, and the ridge itself, whose step profile is the page's only drawn landscape.

### Named Rules
**The Square Corner Rule.** Zero radius on every surface, control, and plate. A rounded corner is a different world.

**The Pixelated Rule.** Any raster of the mascot or mark is scaled with `image-rendering: pixelated`. Never let a pixel asset interpolate.

## Components

### Buttons
- **Shape:** square (0 radius), 1px border, no shadow.
- **Primary:** rust fill, `#150609` text, 700 weight at 0.9375rem, `0.7rem 1.1rem` padding, 1px rust border. Hover swaps both fill and border to Rust Glow. The HUD variant is the same plate at `0.5rem 1rem` with `min-height: 2.75rem`.
- **Secondary:** transparent fill, 1px `--line-2` border, bone text. Hover fills `--ink-3` and keeps the border. Used for "View source" and npm.
- **Focus:** a 2px `--focus` outline at 3px offset, applied globally via `:focus-visible`; buttons do not define their own ring.
- **Icons:** 1rem inline SVG with `stroke-linecap: square`; the GitHub mark is filled.

### Chips (tool tags)
- **Style:** `--ink-3` fill, 1px `--line` border, bone text at 0.75rem in monospace, `0.22rem 0.5rem` padding, square corners.
- **Use:** the tool names under a stage's prose (`lsp`, `ast_edit`, `read`, `debug`). They are labels, not filters — no hover or selected state.

### Cards / Containers
- **Corner Style:** none.
- **Background:** `--ink-2` for raised plates, `--ink` for card bodies inside a bordered pair.
- **Border:** 1px `--line-2` outer, 1px `--line` internal seams.
- **Shadow Strategy:** none — see Elevation & Depth.
- **Internal Padding:** 1.25rem for install cards, 1.75rem at 75rem, 1rem 1.1rem for alternative install cards.

### Navigation
The HUD is a fixed bar, 3.75rem tall (3.25rem below 30rem), with a 1px bottom seam and an opaque `--ink` fill — no blur. It carries the pixel mark and Silkscreen "MARS" wordmark, a five-segment stage bar with a live Silkscreen label, section links (dust at rest, bone on hover with an `--ink-3` fill, bone when `aria-current`), and the rust install plate. Below 56rem the section links disappear and the CTA takes the right edge; below 34rem the track label is dropped and the bar segments narrow.

The stage trail below the hero is a second navigation: a horizontal rail on `--ink-2`, each stop separated by a 1px right seam, with a pennant flag, a Silkscreen numeral in Rust Glow, and a name in Anybody. The current stop gets bone text, a rust flag, and a 2px rust underline sitting on the rail's bottom seam. The rail fades only on a side that is actually clipped — the `data-edge` attribute is measured from `scrollLeft`, so a fully visible first or last label is never dimmed.

### Installer Panel (signature)
The page's working action, shown in its working form rather than described.
- **Frame:** 1px `--line-2`, `--ink-2` body, `--ink-3` head bar with a 1px bottom seam. In the install band the same plate sits on `--ink` with 0.4rem of padding, so the frame reads as an inset panel.
- **Head:** OS tabs in Silkscreen 0.6875rem uppercase — selected tab takes `--ink-4` fill and a `--line-2` border, unselected is dust on transparent. A filename label (`install.sh` / `install.ps1`) sits right-aligned in monospace and swaps with the tab.
- **Body:** a `$` or `>` sigil in Rust Glow, then the command in monospace bone. The copy action is a `--ink-4` plate separated by a 1px left seam, Silkscreen uppercase, with a 16px inline copy icon.
- **States:** the copy button swaps to "Copied" (`#8ee08e` on `#16201a`) or "Copy failed" (`#ff9d9d` on `#241417`), resets after 1.8s, and updates its `aria-label` to match the visible label. A successful copy also triggers the mascot's hop.
- **Narrow behaviour:** below 30rem the copy plate moves under the command, the filename is dropped, and the command keeps `overflow-wrap: normal` so a URL never breaks mid-token.

### Alternative Install Cards
- **Style:** 1px `--line` border, `--ink` body, Silkscreen heading in dust, command in monospace bone.
- **Command wrapping:** the package id is wrapped in a no-break span so the line wraps at the space before it and never inside the token.
- **Copy action:** deliberately quiet — no plate, transparent background, dust text turning bone on hover, `min-height: 2.75rem` for the tap target. It is the fallback path, so it must not read as a second primary button.

### Spec List
Label/value rows separated by 1px `--line` seams under a 1px `--line-2` top rule. Labels are Anybody at 0.9375rem in dust; values are Silkscreen Metric in bone with tabular figures, and a unit in Anybody 0.8125rem dust follows the number. Rows align baseline, not center.

### Capture Plate
A bordered `--ink-2` figure holding a real product capture: 1px `--line-2` frame, image with a 1px bottom seam, caption in Anybody 0.8125rem dust preceded by a 6px rust square. Captions may contain `code` in bone. No browser chrome, no fake window dots.

### Stage Numeral
A 0.75rem Silkscreen numeral in Rust Glow, floated left inside each stage `h2` with `0.35rem 0.85rem 0 0` of margin, so the heading text wraps around it. It is `aria-hidden`; a visually hidden `Stage 01:` prefix inside the same heading carries the number for assistive technology.

### Motion
Entrances are hard-edged, stepped, and short. The hero headline wipes in with a `steps(7)` clip, the ridge draws itself with `steps(8)`, and the mascot falls and lands with `steps(4)` — all gated on `prefers-reduced-motion: no-preference` and on a `js` class set by the inline script. Capture plates use a separate, slower clip wipe (760ms) so the two effects never read as one. The mascot idles on a 3.2s `steps(2)` two-frame bob. Under reduced motion every animation and transition is cut to 0.001ms and smooth scrolling is turned off.

### Named Rules
**The Steps Rule.** Entrances are clip wipes timed in `steps()` frames. No eased fades, no blur-ins, no parallax on content.

**The Working Action Rule.** The primary action is shown as the real, copyable thing — a command in a bordered plate with a copy button — not as a button that leads to one.

## Do's and Don'ts

### Do:
- **Do** keep every surface square and flat: 0 radius, 1px seams, and the ink ladder for depth.
- **Do** use rust for action and position only — fills, flags, dots, underlines, numerals — and Rust Glow for any rust-colored word.
- **Do** set machine facts (numerals, commands, OS names, file names, labels) in Silkscreen or monospace, and human sentences in Anybody.
- **Do** gate every entrance on `prefers-reduced-motion: no-preference` and on the `js` class, so a no-JS or reduced-motion visitor sees the finished frame.
- **Do** hold prose to 62ch and headlines to 16–22ch.
- **Do** keep every action at least 2.75rem tall — the HUD plate and the quiet copy actions set `min-height: 2.75rem`; the primary and secondary buttons reach it through padding — and give each a visible `:focus-visible` ring in Focus Cyan.
- **Do** let the mascot's feet meet the ridge line at every breakpoint; the ridge is the ground, not a decoration behind the copy.

### Don't:
- **Don't** add a shadow, glow, blur, or `backdrop-filter`. There are none in the build and the world does not have a vocabulary for them.
- **Don't** round a corner, on any element, for any reason.
- **Don't** use a gradient as a surface fill, a text fill, or a control fill. Gradients exist only in the page ground vignette, the 1px star field, the horizon hairline, and the trail's scroll-edge mask.
- **Don't** set body copy in rust. Mars Rust on Ground Ink is 4.60:1 — it is a mark color, not a reading color.
- **Don't** use Focus Cyan for anything but the focus ring.
- **Don't** introduce a second accent hue, a warm neutral, or a "brand gradient".
- **Don't** ease an entrance. Stepped frames only.
- **Don't** put a kicker, eyebrow, or all-caps label above a headline — the stage numeral inside the heading is the only heading marker this world uses.
