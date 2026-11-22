# Mars Website and Installers

Official website and installer distribution for [Mars Coding Agent](https://github.com/MarsAI-org/mars-agent).

Live site: [https://getmars.eu.cc](https://getmars.eu.cc)

## Installation

### POSIX (Linux, macOS)
```bash
curl -fsSL https://getmars.eu.cc/install | sh
```

### Windows (PowerShell)
```powershell
irm https://getmars.eu.cc/install.ps1 | iex
```

## Install directory

The installers place the `mars` binary in a default location and fall back to an
environment variable override:

- POSIX: `~/.local/bin`
- Windows: `%LOCALAPPDATA%\mars`

Set `MARS_INSTALL_DIR` to install somewhere else. `PI_INSTALL_DIR` is still
honored as a legacy fallback, but new scripts and docs should use
`MARS_INSTALL_DIR`.

## Installer output

Both installers print a step line for each phase (fetch release, download,
verify checksum, install) and print the downloaded size once the transfer
finishes:

- POSIX (`install`): shows a `curl --progress-bar` meter when stderr is a TTY,
  and stays line-oriented when piped (`curl ... | sh`) so output is not
  corrupted by control characters.
- Windows (`install.ps1`): relies on `Invoke-WebRequest`'s built-in progress
  bar, and always prints the byte count of the downloaded binary.

## Development

`index.html` is a single self-contained page with an inline `<style>` block and
no build step. Brand assets live in `assets/` and are also served from the site
root (`/favicon.ico`, `/favicon.svg`, `/favicon-32x32.png`). Type is
self-hosted from `assets/fonts/` (Hanken Grotesk and Spline Sans Mono under the
SIL Open Font License 1.1, see `assets/fonts/OFL.txt`), so the page makes no
third-party requests. The Pages workflow in `.github/workflows/pages.yml` stages
`index.html`, the installers, `CNAME`, `LICENSE`, root favicons, and `assets/`
(excluding provenance sidecar JSON files) into `_site`.

The page is laid out as an **Editorial Instrument** sheet anchored to the
pixel-art Mars mark: warm alabaster ground (`#faf8f5`), crisp white plates,
hairline dividers, obsidian ink (`#161419`), and Mars terracotta orange
(`#d64a27` / `#b43618`) as the sole accent. It ships a 5-method install
workbench (`macOS & Linux`, `Windows`, `Bun`, `Nix`, `mise`), zoomable real TUI
captures under `assets/proof-*.webp` (from `mars-agent/assets/`), a searchable
capability ledger, and live CLI flag composition. `assets/og-image.png` is
rendered from `.og-card.html`, which is a build-time helper and not published.

`DESIGN.md` records the page's design system; `PRODUCT.md` records the product
truth it must not contradict. `.impeccable/review/` holds the last screenshot
pass and is git-ignored.

## Credits

Mars is a fork of oh-my-pi by can1357, which is a fork of Pi by Mario Zechner. Both are MIT licensed.

Hanken Grotesk (Omnibus-Type) and Spline Sans Mono (Sorkin Type) are distributed under the SIL Open Font License 1.1.
