# Smash&Clash — Official Installers

Native installers for **Smash&Clash**, the official strategic card-battle game.
Play it free in your browser at **[smashandclash.in](https://www.smashandclash.in)** —
or install it as a native app below.

> This repository contains **only the installers** — no source code. The game is
> proprietary; see [LICENSE](LICENSE).

## ⬇️ Download

Get the latest installers from the **[Releases page →](https://github.com/smashandclash/installers/releases/latest)**

| Platform | File | Notes |
|---|---|---|
| 🪟 **Windows 10/11 (64-bit)** | `Smash-and-Clash-<version>-Windows-Setup.exe` | Per-user installer, no admin needed |
| 🤖 **Android 7.0+ (API 24+)** | `Smash-and-Clash-<version>-Android.apk` | Sideload; also coming soon on Google Play |

## 🪟 Installing on Windows

1. Download `Smash-and-Clash-<version>-Windows-Setup.exe`.
2. Run it. Because the installer isn't code-signed yet, Windows SmartScreen may
   show **"Windows protected your PC"** — click **More info → Run anyway**.
3. It installs for the current user (no admin prompt) and adds a Start-menu
   shortcut. The WebView2 runtime is installed automatically if missing.

## 🤖 Installing on Android

1. On your phone, download `Smash-and-Clash-<version>-Android.apk`.
2. When prompted, allow installing from this source (**Settings → Allow from
   this source / Install unknown apps**).
3. Open the downloaded file to install, then launch **Smash&Clash**.

> Prefer the Play Store? A Google Play listing is on the way — pre-registration
> coming soon.

## 💻 System requirements

- **Windows:** Windows 10 or 11, 64-bit. (Microsoft Edge WebView2 runtime —
  bundled/auto-installed.)
- **Android:** Android 7.0 (Nougat, API 24) or newer.
- A GPU with WebGL support (virtually all modern devices).

## 🔒 Verify your download (optional)

Each release lists SHA-256 checksums. To verify:

```powershell
# Windows (PowerShell)
Get-FileHash .\Smash-and-Clash-1.0.0-Windows-Setup.exe -Algorithm SHA256
```
```bash
# Android APK (any machine)
sha256sum Smash-and-Clash-1.0.0-Android.apk
```

## ℹ️ About

Smash&Clash is the **official** edition of the game — 51 unique character cards,
a 3×5 board, smash-style captures, an adaptive AI opponent, local hot-seat PvP,
a tutorial, and a mutators mode, with 3D presentation and character voices.

Official site: <https://www.smashandclash.in>

© Smash&Clash. All rights reserved. See [LICENSE](LICENSE).
