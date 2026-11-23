# Mars Website and Installers

Official website and installer distribution for [Mars Coding Agent](https://github.com/MarsAI-org/mars-agent).

Live site: [https://getmars.eu.cc](https://getmars.eu.cc)

## Installation

### POSIX (macOS & Linux)

```sh
curl -fsSL https://getmars.eu.cc/install | sh
```

### Windows (PowerShell)

```powershell
irm https://getmars.eu.cc/install.ps1 | iex
```

Both scripts mirror `scripts/install.sh` and `scripts/install.ps1` in [MarsAI-org/mars-agent](https://github.com/MarsAI-org/mars-agent) and also support building from GitHub source via `--source` / `-Source` (with optional `--ref <ref>` / `-Ref <ref>`). On the site itself, the 4-method install workbench covers `macOS & Linux`, `Windows`, `Nix`, and `mise`.

## Install directory and verification

The installers place the `mars` binary in a default location unless overridden:

- POSIX: `~/.local/bin`
- Windows: `%LOCALAPPDATA%\mars`

Set `MARS_INSTALL_DIR` to install somewhere else (`PI_INSTALL_DIR` is still honored as a legacy fallback, but new scripts and docs should use `MARS_INSTALL_DIR`).

Downloads are verified **fail-closed** against `SHA256SUMS.txt` published alongside each [GitHub Release](https://github.com/MarsAI-org/mars-agent/releases):

- Each binary is downloaded to a staged file beside the destination, verified against `SHA256SUMS.txt`, and smoke-tested with `--version` before being swapped into place (leaving any previous install untouched on failure).
- Checksum mismatches always abort. If `SHA256SUMS.txt` cannot be fetched or no local SHA-256 tool (`sha256sum`/`shasum`) is available, the installer refuses to proceed unless `MARS_ALLOW_UNVERIFIED=1` is set explicitly.

## Installer output

Both installers print a step line for each phase (fetch release, download, verify checksum, install) and print the downloaded size once the transfer finishes:

- POSIX (`install`): shows a `curl --progress-bar` meter when stderr is a TTY, and stays line-oriented when piped (`curl ... | sh`) so output is not corrupted by control characters.
- Windows (`install.ps1`): relies on `Invoke-WebRequest`'s built-in progress bar, and always prints the byte count of the downloaded binary.

## Development

`index.html` is a single self-contained page with inline CSS/JS and no build step. Brand assets live in `assets/` and are also served from the site root (`/favicon.ico`, `/favicon.svg`, `/favicon-32x32.png`). Type is self-hosted from `assets/fonts/` (Hanken Grotesk and Spline Sans Mono under the SIL Open Font License 1.1; see [assets/fonts/OFL.txt](assets/fonts/OFL.txt)), so the page makes no third-party requests.

### Local preview

Serve the repository over HTTP rather than opening `index.html` via `file://` (which breaks the root-absolute `/favicon*` links):

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

### Publishing

The Pages workflow in [.github/workflows/pages.yml](.github/workflows/pages.yml) deploys on push to `main` and stages only the published subset into `_site`:

- Root files: `index.html`, `install`, `install.ps1`, `CNAME`, `LICENSE`, `favicon.ico`, `favicon.svg`, `favicon-32x32.png`
- Assets: `assets/` excluding `assets/*.webp.json` (provenance sidecars), `assets/paper-grain.webp`, and `assets/skyline.svg`
- Never published: `DESIGN.md`, `PRODUCT.md`, `README.md`, `.og-card.html`, and `.impeccable/`

### Design and product docs

The page is laid out as an **Editorial Instrument** sheet anchored to the pixel-art Mars mark: warm alabaster ground (`#faf8f5`), crisp white plates, hairline dividers, obsidian ink (`#161419`), and Mars terracotta orange (`#d64a27` / `#b43618`) as the sole accent. It ships a 4-method install workbench (`macOS & Linux`, `Windows`, `Nix`, `mise`), zoomable real TUI captures under `assets/proof-*.webp` (sourced from `mars-agent/assets/`), a searchable capability ledger, and live CLI flag composition. `assets/og-image.png` is rendered from `.og-card.html` at build time.

[DESIGN.md](DESIGN.md) records the page's design system; [PRODUCT.md](PRODUCT.md) records the product truth it must not contradict. `.impeccable/review/` holds the last screenshot pass and is git-ignored.

## Credits

Mars is a fork of [oh-my-pi](https://github.com/can1357/oh-my-pi) by [can1357](https://github.com/can1357), which is a fork of [Pi](https://github.com/badlogic/pi-mono) by [Mario Zechner](https://github.com/mariozechner). Both are MIT licensed.

Hanken Grotesk (Omnibus-Type) and Spline Sans Mono (Sorkin Type) are distributed under the SIL Open Font License 1.1.
