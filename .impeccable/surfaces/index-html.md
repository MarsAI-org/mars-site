---
version: 2
slug: "index-html"
primary_target: "index.html"
related_targets: []
---

# Landing page — getmars.eu.cc

## Scope

Single route, `/`. Mode: **Persuade**. The visitor is a developer evaluating a
coding agent with their terminal already open; the page's success is an install
command copied.

## Audience and job

Developers on macOS, Linux or Windows arriving from GitHub or a colleague's
link. They need to know what Mars is, why it differs, and how to install it —
inside one viewport.

## Action and proof

Primary action: the working install command, switchable between POSIX and
Windows, pre-selected from the platform, with copy feedback. Secondary: Releases,
npm, Bun, Nix, mise. Proof is the real product: TUI captures plus repository
facts (75 providers, 36 tools, ~240k Rust lines, 12 crates, 6 targets, MIT).

## Constraints

Single static `index.html`, inline CSS and JS, no build step, GitHub Pages.
Logo and name are fixed. Installer URLs, paths and flags are product truth.
Version numbers must not lead the page.

## Direction contract

THESIS: The page is `mars(1)` — the product's own man page, printed on reference
stock. It refuses both the dark terminal-and-neon hero and the equal-card grid,
and it makes the manual the marketing.

OWN-WORLD: Uncoated stock `#f2efe7` with ink `#131110`; rubber-stamp red
`#bf2f1c` as the single accent, carried by rules, markers and the stamp; hairline
rules `#c9c3b6`. Archivo variable: compressed caps for display and section
markers, normal width for reading. Man-page grammar only — a bold left section
ladder with a vertical rule, indented bodies, literal tokens in bold, monospace
only for code. No cards, no shadows, no rounded corners, no glow.

STORY: This is a serious native tool that documents itself precisely and is
confident enough to sign its own sheet. The visitor reads a specification, trusts
it, and presses the stamp to copy the command.

FIRST VIEWPORT: A drawn title block: MARS in compressed caps with the section
suffix `(1)`, a ruled meta column (issue, licence, targets, core) and a red
round approval stamp. Under it, NAME on one line with the definition, then
SYNOPSIS holding the live installer at full width — tabs, command, stamp-shaped
COPY — plus the path, privilege and script note. Sheet colophon at the foot of
the page.

FORM: Chosen world, assigned by the roll; seed: 482115d03558fcc2

FINISH: unreviewed and undocumented is unfinished; this build ends with the
finish review, the verdict, DESIGN.md, and every shipping raster carrying its
provenance.
