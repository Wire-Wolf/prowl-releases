<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/wirewolf-lockup-dark.png">
  <img alt="WireWolf" src="assets/wirewolf-lockup-light.png" width="460">
</picture>

<h1>PROWL</h1>

<p><strong>The intelligent pentester terminal.</strong></p>

<p>Real PTY terminals · a one-click Kali toolbox · an AI co-pilot that remembers every target — all in one window.</p>

<p>
  <a href="https://github.com/Wire-Wolf/prowl-releases/releases/latest"><img alt="Download for Windows" src="https://img.shields.io/badge/Download-Windows-0a0b0d?style=for-the-badge&logo=windows&logoColor=aaff00"></a>
  &nbsp;
  <a href="https://github.com/Wire-Wolf/prowl-releases/releases/latest"><img alt="Download for macOS" src="https://img.shields.io/badge/Download-macOS-0a0b0d?style=for-the-badge&logo=apple&logoColor=aaff00"></a>
</p>

<p>
  <img alt="Windows and macOS" src="https://img.shields.io/badge/Windows_·_macOS-3b3f45?style=flat-square&labelColor=0a0b0d">
  <img alt="Free" src="https://img.shields.io/badge/free-aaff00?style=flat-square&labelColor=0a0b0d">
  <img alt="Needs Docker running" src="https://img.shields.io/badge/needs-Docker_running-2496ED?style=flat-square&logo=docker&logoColor=white">
</p>

</div>

---

## What is PROWL?

A desktop app that keeps pentesters **in flow**. Real terminals (local + a one-click Kali container), an AI co-pilot with **persistent per-target memory**, auto-journaling after key commands, a findings tracker, methodology checklists, a credential vault, and clean engagement notes — so you never lose context between sessions.

## ⬇&nbsp; Download &amp; run

Grab the latest build from the **[Releases page »](https://github.com/Wire-Wolf/prowl-releases/releases/latest)**

| Platform | File | How to run |
|---|---|---|
| **Windows** | `Prowl-x.x.x-portable.exe` | Double-click — no installer, no setup |
| **macOS** | `Prowl-x.x.x.dmg` | Open the dmg, drag Prowl to Applications |

## Requirements

- **[Docker Desktop](https://www.docker.com/products/docker-desktop/)** installed and running — powers the Kali toolbox via the app's one-click **"Pull Pre-built"** button.
- Everything else (terminals, notes, findings, timeline) works with **no** setup at all.

## First launch

PROWL isn't code-signed yet, so your OS shows a **one-time** prompt:

- **Windows** — SmartScreen *"unknown publisher"* → click **More info → Run anyway**.
- **macOS** — Gatekeeper blocks it → **System Settings → Privacy &amp; Security → Open Anyway**, or run `xattr -cr /Applications/Prowl.app` in Terminal, then open it.

## Updates

PROWL shows an in-app **"Update available"** banner when a newer build lands — click it to download the new file. (Portable / dmg builds don't self-install.)

<br>

<div align="center">

**PROWL** — a <a href="https://github.com/Wire-Wolf">WireWolf</a> project · <em>Unified Security</em>

<sub>Only use PROWL on systems you are authorized to assess.</sub>

</div>
