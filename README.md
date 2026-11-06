# Glance Platform

One manager for clean, movable desktop tiles.

**[Download Glance Platform 1.6.0](https://github.com/Brusko25/Glance-Platform-Releases/releases/tag/v1.6.0)** · [User guide](USER_GUIDE.md) · [Release notes](CHANGELOG.md)

Glance Platform brings Finance, LLM Usage, Plex, Investments, Weather, Storage, System Resources, Clock and Notes into a shared desktop tile system. Liquid Icons adds optional liquid and sharp glass backgrounds behind Windows desktop icons, which snap together and jiggle when you drop an icon. Tiles have matching options and right-click menus and run independently. The manager handles installation, placement, the tray and a local Marketplace.

![Glance tiles snapped together on the desktop](images/v1.6.0/desktop.png)

## Get started

1. Download **Glance-Platform-1.6.0-Setup.exe** from the release page. If Glance is running, choose Quit Glance before running Setup.
2. Run setup to install Glance for your Windows account, with a Start menu entry and an optional desktop shortcut.
3. If Windows asks for administrator permission for the bundled CPU sensor, approve it to show CPU temperature in Plex. Glance installs either way, and you can add the sensor later with Settings → Repair CPU temperature.
4. Open Glance from the Start menu or its shortcut and install the tiles you want from Marketplace.

Prefer a portable copy? Download the Windows ZIP, extract the entire folder, and run Start Glance.cmd. Try Glance.cmd opens sample tiles in a separate workspace.

Requires Windows 10/11 and .NET Framework 4.8. The installer and portable ZIP are unsigned. Setup registers Glance in Windows Installed apps / Add or remove programs; uninstall keeps your saved tile data.

## Included

| Tile | Based on |
| --- | --- |
| Finance | Glance Finance 2.6.6 |
| LLM Usage | Glance LLM Usage 2.2.1 |
| Plex | Glance Plex 2.3.0 |
| Investments | Webull balances, holdings and open P/L through your own Webull API keys |
| Local Weather | Worldwide city or postal-code search, current conditions and a 10-day forecast |
| Storage | Every internal and USB drive with a usage bar and its free space |
| System Resources | CPU, memory, GPU, network and disk activity, turning amber and red when something is working hard |
| Clock and Notes | Local time and a saved scratchpad |
| Liquid Icons | Optional liquid and glass backgrounds that flow together around desktop icons |

Included tile versions are Finance 1.5.0, LLM Usage 1.5.0, Plex 1.5.0, Investments 1.3.0, Local Weather 1.2.0, Clock 1.5.0, Notes 1.5.0, Liquid Icons 1.4.0, Storage 1.1.0 and System Resources 1.1.0. The installer and Windows ZIP include all ten tile packages. Separate Finance, Usage and Plex packages, a creator kit in the ZIP, and SHA-256 checksums are also provided.

**Settings → Platform updates** checks GitHub for the main app. **My Tiles → Update all installed tiles** installs newer bundled or local catalog packages while preserving settings and positions. Platform updates refresh existing Glance shortcut icons and apply newer bundled tiles when their automatic-update preference is enabled.

Every bundled tile has a 75%–200% scale slider in its options. Plex reads CPU temperature through the included sensor component without a separate monitoring app, showing Celsius to the left of Fahrenheit. Windows administrator permission is required to set up that component; readings depend on CPU support.

**Options → Style** offers ready-made looks (Classic, Compact Grey, Midnight, Neon, Paper and more), background colours, borders and corner shapes. Preview your choices, then apply them to one tile or all installed tiles. Accounts, notes, locations and desktop positions stay unchanged. Shared Desktop controls and tile-specific tabs follow the Finance options layout. Minimize tucks the manager into the tray beside the clock. Your account connections and saved tile data stay on your PC.

Investments requires your own approved Webull API access for Webull syncing.

## Create tiles with AI

Describe the tile you want in **Create Tiles → Create with AI** and choose **Copy AI prompt**. Paste it into any AI chat, such as ChatGPT, Claude or Gemini; the prompt tells the AI everything it needs about Glance tiles. Then choose **Build from AI reply…** and paste the answer. Glance compiles it on your PC, checks it and adds it to your Marketplace, where you review what it can access before installing. If the build fails, one click copies the errors back for the AI to fix. AI-written tiles run with your Windows account's access, like any tile.

Marketplace currently browses bundled tiles and a local catalog. Public submissions and online tile hosting are planned. This repository hosts public documentation and release downloads; application implementation is maintained separately.

## Screenshots

Real captures of Glance Platform 1.6.0 on Windows 11. The tiles use the Classic layout with a black background, rounded corners and **Merge snapped tiles**, so touching tiles share one outline. All names, drives, streams, accounts and usage are sample data; the market charts and the Seattle weather were live public data at capture time.

![Glance Plex with three streams and Tdarr working](images/v1.6.0/plex.png) ![System Resources over LLM Usage](images/v1.6.0/system-usage.png) ![Storage](images/v1.6.0/storage.png) ![Investments over Weather](images/v1.6.0/investments-weather.png)

![Finance charts snapped in a row](images/v1.6.0/finance.png)

![Glance window: My Tiles](images/v1.6.0/manager.png)
![Glance window: Marketplace](images/v1.6.0/marketplace.png)
![Glance window: Style for all tiles](images/v1.6.0/style.png)
![Glance window: Settings and Platform updates](images/v1.6.0/settings.png)

![System Resources options](images/v1.6.0/system-options.png)
![Liquid Icons glass presets with synthetic desktop icons](images/v1.6.0/liquid-icons.png)

![Create with AI](images/v1.6.0/create.png)
![Building a tile from an AI reply](images/v1.6.0/ai-build.png)
