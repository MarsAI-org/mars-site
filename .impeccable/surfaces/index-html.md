---
version: 1
slug: "index-html"
primary_target: "index.html"
related_targets: []
---

# Landing page — getmars.eu.cc

## Scope

Single route, `/`. Mode: **Persuade**. The visitor is a developer evaluating a
coding agent with their terminal already open; the page's success is an install
command copied or a binary downloaded.

## Audience and job

Developers on macOS or Linux (sometimes Windows or Termux) arriving from GitHub
or a colleague's link. They need to know what Mars is, why it differs from other
agents, and how to install it — in that order, within one viewport.

## Action and proof

Primary action: the working install command, switchable between POSIX and
Windows, with copy feedback. Secondary: GitHub Releases, npm, Bun, Nix, mise.
Proof is the real product: TUI captures from `mars-agent/assets/`, plus measured
repository facts (75 providers, 36 built-in tools, ~240k Rust lines, 12 crates,
6 release targets, MIT). No customer logos or benchmarks exist; do not invent.

## Constraints

Single static `index.html`, inline CSS and JS, no build step, GitHub Pages.
Logo and name are fixed. Installer URLs, paths, and flags are product truth.
Version numbers must not lead the page: the npm registry and GitHub Releases
disagree.

## Direction contract

THESIS: The page is a surface traverse — a pixel-art planet standing on a chunky
ridge, with each capability as a stage you clear. It refuses the category's dark
terminal-screenshot hero and equal-card grid.

OWN-WORLD: Near-black ground (#0a090d) with a Mars-rust ink (#d64a27) that owns
the mascot, the active stage, and the primary action; bone (#f4ece2) type; dust
(#ada4ad) secondary; a single cool cyan only for focus. Anybody (variable, wide)
carries voice; Silkscreen is the machine voice on numbers, labels, and commands.
Surfaces are flat, separated by 1px lines and 2px strokes — no glass, no glow,
no gradient text. Pixel blocks and 4px increments are the only decoration.

STORY: This is a serious native tool that is also fun to run. The visitor sees a
creature standing on a planet, understands that the agent works inside the
editor's real machinery, and copies a command.

FIRST VIEWPORT: HUD with the pixel mark and a five-segment stage bar. Headline
left at 80px, lede below, then the live installer with OS tabs and a copy button,
then four meta facts. The mascot stands at the right, its feet on the ridge; the
ridge and the stage trail close the viewport. Primary action sits above the fold.

FORM: Chosen world, top of the ordered list. seed: c8032afaaa3595c6

FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance.
