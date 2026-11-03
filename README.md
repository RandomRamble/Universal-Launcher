# Universal Launcher
This originally had tons of bugs but I fixed it.
An offline-first Minecraft launcher for Windows. Link an existing Minecraft folder and play right away — no re-downloading, no Microsoft account, no ads, no telemetry. Everything runs locally on your machine.

[License](https://img.shields.io/badge/license-GPL--3.0-blue) [Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-0078d6) [Built with](https://img.shields.io/badge/built%20with-Electron-9cf)

## Why Universal Launcher

Most launchers force you to re-download gigabytes of game files or log in with a Microsoft account. Universal Launcher takes the opposite approach:

- **Link, don't download.** Point the launcher at an existing Minecraft installation folder (official launcher, SKLauncher, or any compatible layout) and it resolves everything locally — versions, libraries, assets, and the client jar. Zero downloads, even when Mojang's servers are down.
- **Private by design.** Offline accounts (no Microsoft login), no ads, no analytics, no tracking. Your data never leaves your computer.
- **Loader support.** Vanilla, Fabric and Quilt (500+ merged versions), plus Forge / NeoForge latest auto-detect.
- **Clean custom UI.** Dark, minimal, borderless design with per-instance custom icons, including your own icon on the Windows taskbar and launcher executable.

## Features

| **Feature** | **Description** |
|---|---|
| Offline launch | Client jar resolved from your existing folder; system Java auto-detected (`JAVA_HOME` → `PATH`) with version verification before any download is attempted |
| Link existing folder | Use any compatible Minecraft directory as-is; game files are never copied or modified |
| Download & install | Classic flow to download a fresh instance when Mojang services are reachable |
| Merged versions | Fabric & Quilt version lists merged and deduplicated into one picker |
| Forge / NeoForge | "Latest (auto-detect)" support |
| RAM control | Per-instance or global RAM (default 4 GB, 256 MB steps); smart heap sizing (`-Xms`) so the game starts with the memory you set |
| Mod-friendly | Loads your existing mods folder as-is (tested with Sodium, Iris, Lithium, JEI, Xaero's) |
| Offline accounts | Multiple local profiles, no Microsoft authentication required |
| Custom icons | Per-instance icons, taskbar app icon, and executable icon |
| No administrator required | Runs without administrator permissions or an elevated installation |
| Portable executable | Distributed as a single `.exe` file |

## Requirements

- Windows 10 / 11 (64-bit)
- Java 17+ recommended. If Java is missing, the launcher falls back to a detected system JVM (`JAVA_HOME` → `PATH`) and only attempts a runtime download when nothing is available and Mojang's services are reachable.
- An existing Minecraft installation (optional) used by the link existing folder flow. Without one, use Download & install.

## Installation

1. Download **Universal Launcher.exe** from the [Releases](https://github.com/thewoldaa/vertal-launcher/releases) page.
2. Run the executable. No administrator permissions required.
3. Open Universal Launcher and create your first instance.

That's it. No Node.js, npm, additional dependencies, or traditional installation process required.

## Getting Started

### 1. Link an existing folder (recommended)

1. Go to Instances → New Instance.
2. Choose "Use existing folder" and select your Minecraft directory (e.g. one created by the official launcher or SKLauncher).
3. The launcher automatically detects the game version and loader profile (e.g. Minecraft 26.1.2 + Fabric 0.19.3).
4. Set the memory you want (or leave it on Global) and click Launch.

### 2. Download & install

1. Go to Instances → New Instance → "Download & install".
2. Pick a version and loader from the pickers.
3. The launcher downloads the version metadata, libraries, and client jar (requires Mojang services to be reachable).

### 3. Profiles & RAM

- Create multiple offline profiles without a Microsoft account.
- Set per-instance RAM or leave it on Global (managed in Settings, default 4 GB).
- The readout shows "Global (X GB from Settings)" so you always know how much memory will be used.

## Technology

- [Electron](https://www.electronjs.org/) — desktop application framework.
- Vanilla HTML / CSS / JavaScript — no frontend framework.
- Distributed as a standalone Windows executable.

## Supporting the Project

Universal Launcher is free, open source, and ad-free. If it saves you time or bandwidth, consider supporting its development:

- Star the repository.
- Report bugs or suggest features.
- Open a pull request — contributions are welcome.

## Contributors

- CraftKal — creator & maintainer · [github.com/craftkal](https://github.com/craftkal)
- thewoldaa — maintainer · [github.com/thewoldaa](https://github.com/thewoldaa)

Contributions are welcome. Open an [issue](https://github.com/thewoldaa/vertal-launcher/issues) or submit a pull request.

## License

[GNU General Public License v3.0](https://github.com/thewoldaa/vertal-launcher/blob/main/LICENSE) © 2026 CraftKal

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version. It is distributed in the hope that it will be useful, but without any warranty; see the `LICENSE` file for the full text.

---

Universal Launcher is an independent project and is not affiliated with Mojang Studios or Microsoft. Minecraft is a trademark of Mojang Synergies AB.
