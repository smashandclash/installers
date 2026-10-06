# Smash&Clash — Official Installers

[![skills.sh](https://skills.sh/b/smashandclash/plugin)](https://skills.sh/smashandclash/plugin)

Native installers for **Smash&Clash**, a two-player strategy board game where every move matters. Play it free in your browser at **[smashandclash.in](https://www.smashandclash.in)**, or install it as an app below.

> This repository contains **only the installers**, no source code. The game is proprietary; see [LICENSE](LICENSE).

## Download

The latest release is **2.1.0**: [Windows](https://github.com/smashandclash/installers/releases/download/v2.1.0/Smash-and-Clash-2.1.0-Windows-Setup.exe) · [macOS](https://github.com/smashandclash/installers/releases/download/v2.1.0/Smash-and-Clash-2.1.0-macOS-Universal.dmg) · [Linux AppImage](https://github.com/smashandclash/installers/releases/download/v2.1.0/Smash-and-Clash-2.1.0-Linux-x86_64.AppImage) · [.deb](https://github.com/smashandclash/installers/releases/download/v2.1.0/Smash-and-Clash-2.1.0-Linux-amd64.deb) · [.rpm](https://github.com/smashandclash/installers/releases/download/v2.1.0/Smash-and-Clash-2.1.0-Linux-x86_64.rpm) · [Android APK](https://github.com/smashandclash/installers/releases/download/v2.1.0/Smash-and-Clash-2.1.0-Android.apk) · [SHA256SUMS.txt](https://github.com/smashandclash/installers/releases/download/v2.1.0/SHA256SUMS.txt)

Every release is on the **[Releases page](https://github.com/smashandclash/installers/releases/latest)**.

| Platform | File | Notes |
|---|---|---|
| **Windows 10/11 (64-bit)** | `Smash-and-Clash-<version>-Windows-Setup.exe` | Per-user installer, no admin needed |
| **macOS 11+** | `Smash-and-Clash-<version>-macOS-Universal.dmg` | One app for Apple Silicon and Intel |
| **Linux** | `Smash-and-Clash-<version>-Linux-x86_64.AppImage` | Any distribution; also `.deb` (Debian/Ubuntu) and `.rpm` (Fedora/openSUSE) |
| **Android 7.0+** | `Smash-and-Clash-<version>-Android.apk` | Sideload, or get it on Google Play |
| **iPhone / iPad** | (no file) | Add the web app to your Home Screen (see below) |

Each release lists SHA-256 checksums in `SHA256SUMS.txt`.

## What's new in 2.1.0

**Every client plays every other.** Smash&Clash is one game network, and these apps are part of it:

- **Play a friend** makes a room with a six-letter code. Your friend joins with that code from anywhere: these apps, [smashandclash.in](https://www.smashandclash.in), Telegram, a terminal (`npx smashandclash open CODE`) or any app built on the [SDK](https://docs.smashandclash.in/sdk). Codes from all of those work here too.
- **Quick match** pairs you with players on every client, not only other app players.
- Games connect on any network, including mobile data, and stay fair: the game network checks every move.

More in the docs: [one game, every client](https://docs.smashandclash.in/clients).

## Windows

1. Download `Smash-and-Clash-<version>-Windows-Setup.exe` and run it.
2. The installer isn't code-signed yet, so Windows SmartScreen may show **"Windows protected your PC"**. Click **More info → Run anyway**.
3. It installs for the current user (no admin prompt) and adds a Start-menu shortcut. The WebView2 runtime is installed automatically if it's missing.

## macOS

1. Download `Smash-and-Clash-<version>-macOS-Universal.dmg`, open it, and drag **Smash&Clash** into **Applications**.
2. The app isn't notarized by Apple yet. The first time, **right-click (or Control-click) the app → Open**, then confirm **Open**. After that it opens normally.
   - On recent macOS versions you may instead see "Smash&Clash can't be opened". If so, go to **System Settings → Privacy & Security** and click **Open Anyway**.

## Linux

- **AppImage (any distribution):**
  ```bash
  chmod +x Smash-and-Clash-<version>-Linux-x86_64.AppImage
  ./Smash-and-Clash-<version>-Linux-x86_64.AppImage
  ```
- **Debian / Ubuntu:** `sudo apt install ./Smash-and-Clash-<version>-Linux-amd64.deb`
- **Fedora / RHEL / openSUSE:** `sudo dnf install ./Smash-and-Clash-<version>-Linux-x86_64.rpm`

The app uses the system WebKitGTK (webkit2gtk 4.1), which the `.deb` and `.rpm` pull in automatically.

## Android

- **Google Play:** search for Smash&Clash (rolling out).
- **Sideload:**
  1. On your phone, download `Smash-and-Clash-<version>-Android.apk`.
  2. When prompted, allow installing from this source (**Settings → Install unknown apps**).
  3. Open the downloaded file to install it, then launch **Smash&Clash**.

## iPhone and iPad

Open **[smashandclash.in](https://www.smashandclash.in)** in **Safari**, tap **Share**, then **Add to Home Screen**. It installs as a full-screen app with its own icon, and it plays offline once the offline pack has downloaded. An App Store version will follow.

## Verify your download (optional)

```bash
# macOS / Linux
shasum -a 256 Smash-and-Clash-<version>-*        # compare with SHA256SUMS.txt
sha256sum -c SHA256SUMS.txt --ignore-missing      # Linux
```
```powershell
# Windows (PowerShell)
Get-FileHash .\Smash-and-Clash-<version>-Windows-Setup.exe -Algorithm SHA256
```

## System requirements

- **Windows:** Windows 10 or 11, 64-bit. The Microsoft Edge WebView2 runtime is bundled or auto-installed.
- **macOS:** macOS 11 Big Sur or newer, Apple Silicon or Intel.
- **Linux:** x86_64 with WebKitGTK 4.1 (Ubuntu 22.04+, Debian 12+, Fedora 38+ or equivalent).
- **Android:** Android 7.0 (API 24) or newer.
- **iPhone / iPad:** iOS / iPadOS 16.4 or newer in Safari.
- A GPU with WebGL support (virtually all modern devices).

## For AI agents

Agents can play Smash&Clash too: over MCP at `https://www.smashandclash.in/api/mcp`, with [`npx smashandclash`](https://www.npmjs.com/package/smashandclash), or with the skills:

```bash
npx skills add smashandclash/plugin
```

## About

Smash&Clash is the **official** edition of the game: 51 unique character cards on a 3×5 board, with smash-style captures. It has:

- an adaptive AI opponent;
- online play with players on every client (rooms by code, quick match) and local hot-seat PvP;
- a tutorial and Mutators mode;
- 3D presentation and character voices.

Official site: <https://www.smashandclash.in>

© Smash&Clash. All rights reserved. See [LICENSE](LICENSE).
