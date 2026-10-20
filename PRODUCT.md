# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Developers who already work in a terminal and are evaluating or adopting a coding
agent. They arrive from a GitHub link, a README, or a colleague's recommendation,
usually on macOS or Linux, sometimes on Windows or Android/Termux. Their job in
the first minute is to decide whether Mars is worth installing and, if so, to run
one command.

## Product Purpose

Mars is a coding agent CLI distributed as a prebuilt binary (and via npm, Bun,
Nix, and mise). This site exists to get the visitor from "what is this?" to a
running `mars` binary with the fewest possible steps. Success is a copied or
executed install command.

## Positioning

A coding agent with the IDE wired in. Mars links the tools other agents shell out
for — ripgrep, glob, find, bash, coreutils — into the process as a Rust core, and
routes edits through real language servers and real debuggers. One binary, the
same behavior on macOS, Linux, and Windows, with no WSL bridge.

## Operating Context

Visitors evaluate in a browser tab while their terminal is open. They copy a
POSIX `curl | sh` command or a PowerShell `irm | iex` command, or download an
archive from GitHub Releases. Advanced paths include `bun install -g`, Nix, and
mise. Installers verify checksums, install to `~/.local/bin` or
`%LOCALAPPDATA%\mars`, and report PATH state.

## Capabilities and Constraints

Confirmed product facts:

- 75 providers in the bundled catalog, routed across nine model roles.
- 36 built-in tools.
- Roughly 240k lines of Rust core across twelve crates, with ~50k more vendored
  in-process.
- Six release targets: linux-x64, linux-arm64, darwin-x64, darwin-arm64,
  win32-x64, win32-arm64.
- LSP on every write, including `workspace/willRenameFiles` renames.
- Real debugger support (lldb, dlv, debugpy) through DAP.
- Subagents in isolated worktrees with schema-validated results.
- `/review` with P0–P3 ranking and a verdict; `/collab` shared sessions.
- Persistent Python and JavaScript eval cells that can call back into agent tools.
- `read` handles local paths, archives, SQLite, PDFs, URLs, and internal schemes
  such as `pr://`, `issue://`, `agent://`, `skill://`, `conflict://`.
- Memory the agent curates across sessions; ACP support for Zed.
- MIT licensed. A fork of oh-my-pi by can1357, itself a fork of Pi by Mario
  Zechner.

Constraints:

- Static single-file `index.html` with inline CSS and JS. No build step. Deployed
  by GitHub Pages from `.github/workflows/pages.yml`.
- Installer commands, URLs, and paths are product truth and must stay exact.
- No fabricated customers, benchmarks, prices, or testimonials.
- Version numbers in the UI must come from a verifiable source. GitHub Releases
  and the npm registry currently disagree, so the page should not lead with a
  version claim.

## Brand Commitments

- Name: Mars. Wordmark set as "Mars".
- Logo: the pixel-art Mars planet provided by the user (orange planet, darker
  craters, two square eyes, two feet) on a near-black ground. The supplied PNG is
  the identity reference.
- The visual world is open for exploration; the logo and the name are fixed.
- Upstream credits (oh-my-pi, Pi, their authors, MIT) must remain visible.

## Evidence on Hand

- `mars-site/assets/mars-logo.png` — supplied pixel-art logo (1254×1254 RGB).
- `mars-site/assets/mars-logo.svg`, favicons, `og-image.png` — existing brand files.
- `mars-agent/README.md` — the canonical feature and install copy.
- Real TUI captures available from `mars-agent/assets/`: `lspv.webp`, `task.webp`,
  `review.webp`, `ttsr.webp`, `python.webp`, `arxiv.webp`. They are real product
  screenshots and may be used as proof, subject to file size.
- No customer logos, testimonials, or benchmark results exist. Do not invent any.

## Product Principles

1. One command to running. Every scroll position should make installing easier,
   not just more interesting.
2. Show the mechanism. The argument is the in-process Rust core, the LSP rename,
   the debugger attach — demonstrated, not adjectives.
3. Native, not wrapped. The same binary on every platform is a claim the page
   should make concrete.
4. Honest proof only. Real screenshots, real numbers from the repository, no
   invented social proof.
5. Terminal-native voice. The audience lives in a shell; the page can speak that
   language without becoming a terminal costume.

## Accessibility & Inclusion

No product-specific standard was established. Follow WCAG AA contrast, keyboard
operability, visible focus, reduced-motion support, and semantic landmarks.
