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

## Development

`index.html` is a single self-contained page with an inline `<style>` block and
no build step. Brand assets live in `assets/` and are also served from the site
root (`/favicon.ico`, `/favicon.svg`, `/favicon-32x32.png`). The Pages workflow
in `.github/workflows/pages.yml` copies `index.html`, the installers, `CNAME`,
`LICENSE`, and both asset directories into the `_site` publishing directory.

## Credits

Mars is a fork of oh-my-pi by can1357, which is a fork of Pi by Mario Zechner. Both are MIT licensed.
