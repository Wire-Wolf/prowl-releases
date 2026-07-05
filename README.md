<div align="center">

# Prowl

**An intelligent pentester terminal — real PTY terminals + an AI co-pilot with persistent, per-target memory.**

### [⬇ Download the latest release](https://github.com/Wire-Wolf/prowl-releases/releases/latest)

</div>

---

## Download & run

Grab the latest build from the [**Releases page**](https://github.com/Wire-Wolf/prowl-releases/releases/latest):

- **Windows** — `Prowl-x.x.x-portable.exe` · a single double-click file, no installer.
- **macOS** — `Prowl-x.x.x.dmg`.

### Requirements
- **[Docker Desktop](https://www.docker.com/products/docker-desktop/)** installed and running — Prowl uses it for the Kali toolbox (one-click **"Pull Pre-built"** inside the app). The core app (terminals, notes, findings, timeline) works without it.

### First launch (Prowl isn't code-signed yet)
The OS shows a one-time prompt because the app is unsigned:

- **Windows** — SmartScreen *"unknown publisher"* → click **"More info" → "Run anyway"**.
- **macOS** — Gatekeeper blocks it → **System Settings → Privacy & Security → "Open Anyway"**, or run
  `xattr -cr /Applications/Prowl.app` in Terminal, then open it.

### Updates
Prowl shows an in-app **"update available"** banner when a newer build is out — click it to download the
new file. (Portable / dmg builds don't self-install.)

---

> **Legal**: Only use Prowl on systems you are authorized to assess.
