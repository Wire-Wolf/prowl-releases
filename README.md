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
  <img alt="Free to use" src="https://img.shields.io/badge/free_to_use-aaff00?style=flat-square&labelColor=0a0b0d">
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
| **Windows** (recommended) | `Prowl-Setup-x.x.x.exe` | Installs Prowl — adds a Start Menu + desktop shortcut so you can reopen it anytime |
| **Windows** (portable) | `Prowl-x.x.x-portable.exe` | Runs without installing — a single double-click file (great for a USB stick) |
| **macOS** | `Prowl-x.x.x.dmg` | Open the dmg, drag Prowl to Applications |

### First launch (a one-time OS prompt)

PROWL isn't code-signed yet, so your OS shows a **one-time** "unknown developer" prompt:

- **Windows** — SmartScreen appears → click **More info → Run anyway**.
- **macOS** — Gatekeeper blocks it → open **System Settings → Privacy &amp; Security → Open Anyway**, or run `xattr -cr /Applications/Prowl.app` in Terminal, then open it.

---

## 🐉 Set up the Kali toolbox

PROWL runs 30+ pentest tools (nmap, gobuster, sqlmap, hydra, …) inside a ready-made Kali container — **you don't install any tools yourself.**

1. Install **[Docker Desktop](https://www.docker.com/products/docker-desktop/)** and make sure it is **running** (you'll see the whale icon in your tray/menu bar).
2. In PROWL, click the **Kali icon** in the title bar.
3. Click **"Pull Pre-built"** — this downloads the ready-made Kali image **once** (a few minutes). No building, no configuration.
4. Open a **Kali terminal tab** — the full toolbox is ready to go.

> Only need the basics? PROWL's local terminal, notes, findings, and timeline all work **without** Docker. Docker is only for the bundled Kali tools.

## 🔒 Connect to a VPN (HackTheBox, labs, PortSwigger, …)

To reach a lab network like **HackTheBox**, load your `.ovpn` file into PROWL. The VPN runs **inside the Kali container**, so your Kali terminals route straight to the target box — no host network config, no fiddling with OpenVPN yourself.

1. **Start the Kali container first** — the VPN needs it running. Click the **Kali icon** in the title bar and start the container (see above).
2. **Download your `.ovpn`** from the lab. On HackTheBox: **Connections → download the VPN pack** (`.ovpn`).
3. In PROWL, click the **shield / VPN icon** at the far right of the title bar to open the VPN panel.
4. Click **"Upload .ovpn file"** and pick your config — it opens a normal file picker.
5. **Click the file in the list to connect** (the file row *is* the connect button). It takes ~15 seconds; when it shows **"Connected — &lt;ip&gt;"** and the shield turns green, you're on the VPN.
6. Open a **Kali terminal tab** — it's now on the lab network. Go ahead and `ping` / `nmap` your target.

Switch machines or regions by clicking a different `.ovpn`; disconnect with the **Disconnect** button.

> Works on **Windows &amp; macOS** out of the box — PROWL creates the tunnel device inside the container for you (that's why the Kali container needs to be running first).

## 🤖 Set up the AI co-pilot

On first launch, PROWL walks you through a short setup. Choose **one** of three:

### 🟢 Local AI (Ollama) — free &amp; private · *recommended for most*
Runs entirely on your machine — no account, no API key, no cost.
1. Install **[Ollama](https://ollama.com/download)**.
2. Download a model — in a terminal, run: `ollama pull llama3.1`
3. In PROWL's onboarding (or **Settings**), choose **Local (Ollama)** and pick your model.

### 🔵 Claude — most capable · *needs an API key (pay-as-you-go)*
The smartest option, billed by Anthropic for what you use.
1. Create an account at **[console.anthropic.com](https://console.anthropic.com/)**, add a payment method, and create an **API key**.
2. In PROWL → **Settings**, set the provider to **Anthropic** and paste your key.

### ⚪ No AI
Skip it and use PROWL as a pure operator terminal + note-taking tool.

*You can change your choice anytime in **Settings**.*

---

## ⌨️ Commands

PROWL turns a few plain words typed at the **start of any terminal line** into shortcuts — no slashes, no menus. Type **`help`** at any time to see the full list inside the app.

**Target & recon**
| Command | What it does |
|---|---|
| `target <ip>` | Set the primary target IP — wakes the AI's memory for that box |

**AI co-pilot**
| Command | What it does |
|---|---|
| `ask <question>` | Ask the AI assistant |
| `hack help` | AI pentest methodology guidance |
| `add last <tool>` | Send your last command's output to the AI for analysis |
| `commands <tool>` | Show common commands for a tool (nmap, gobuster, …) |

**Notes & notebooks**
| Command | What it does |
|---|---|
| `note <text>` | Save a quick note (appends to the active notebook) |
| `note #<n> <text>` | Append to note number *n* |
| `notes add <text>` | Append to the active notebook or latest note |
| `notebook <name>` | Set the active notebook for this session |
| `notebook new <name>` | Start a fresh notebook |
| `notebook close` | Stop writing to the active notebook |
| `search <term>` | Search your notes |
| `export notes` | Export all notes to a `.md` file |

**See everything**
| Command | What it does |
|---|---|
| `help` | Show the full command reference inside PROWL |

> Example: type `target 10.10.10.5`, then `ask what should I enumerate first?`

---

## Updates

PROWL shows an in-app **"Update available"** banner when a newer build lands — click it to download the new file. (Portable / dmg builds don't self-install.)

## License

PROWL is **proprietary software** — see **[LICENSE](LICENSE)**. You may download and run the official app for authorized security testing, but you may **not** copy, modify, reverse-engineer, resell, redistribute, or bundle it into any other software or product.

<br>

<div align="center">

**PROWL** — a <a href="https://github.com/Wire-Wolf">WireWolf</a> project · <em>Unified Security</em>

<sub>Only use PROWL on systems you are authorized to assess.</sub>

</div>
