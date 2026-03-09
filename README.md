# Tempo Tokenlist Manager

GUI for managing token submissions to the [Tempo blockchain token list](https://tokenlist.tempo.xyz/list/4217) (Chain 4217 — Presto mainnet).

## Features

- View current tokens on the Tempo mainnet token list
- Add new tokens via form or paste JSON
- Staging area (localStorage-backed) for batch submissions
- Submit PRs to [tempoxyz/tempo-apps](https://github.com/tempoxyz/tempo-apps) via the GitHub API
- Light/dark theme toggle

## Quick Start

1. Clone the repo
2. Copy `config.local.js.example` to `config.local.js` and fill in credentials
3. Open `docs/index.html` in a browser (or deploy via GitHub Pages)

## Project Structure

```
docs/                          # GitHub Pages app
  index.html                   # Single-file app (HTML + CSS + JS)

data/
  staging/4217/
    entries/                   # Staged token entries (one JSON per token)
    icons/                     # Uploaded SVG icons
  archive/4217/                # Archived submissions

scripts/                       # CI helper scripts
.github/workflows/             # GitHub Actions
```

## Local Config

Create `config.local.js` in the project root (gitignored):

```js
window.TEMPO_CONFIG = {
  TEMPO_EXPLORER_USER: '',
  TEMPO_EXPLORER_PASS: '',
  GITHUB_TOKEN: '',
  TEMPO_RPC_URL: '',
};
```

## License

MIT
