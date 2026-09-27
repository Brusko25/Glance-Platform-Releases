# Glance Platform

One manager for clean, movable desktop tiles.

**[Download Glance Platform 1.0.0](https://github.com/Brusko25/Glance-Platform-Releases/releases/tag/v1.0.0)** · [User guide](USER_GUIDE.md) · [Release notes](CHANGELOG.md)

Glance Platform brings Finance, LLM Usage and Plex into a shared desktop tile system. Tiles keep their original options and run independently. The manager handles installation, placement, the tray and a local Marketplace.

## Get started

1. Download Glance-Platform-1.0.0-Windows.zip from the release page.
2. Extract the entire folder.
3. Run Start Glance.cmd for your normal workspace, or Try Glance.cmd for sample tiles.

Requires Windows 10/11 and .NET Framework 4.8. Glance is portable and unsigned; no installer is included.

## Included

| Tile | Based on |
| --- | --- |
| Finance | Glance Finance 2.6.6 |
| LLM Usage | Glance LLM Usage 2.2.1 |
| Plex | Glance Plex 2.3.0 |
| Clock and Notes | SDK examples |

All three converted tile packages are version 1.0.0. The release includes their .glancetile files, a creator kit in the Windows ZIP, and SHA-256 checksums.

Settings opens each tile's familiar options. Minimize tucks the manager into the tray beside the clock. Your account connections and saved tile data stay on your PC.

## Create tiles with AI

Describe the tile you want in **Create tiles → Create with AI** and choose **Copy AI prompt**. Paste it into any AI chat, such as ChatGPT, Claude or Gemini; the prompt tells the AI everything it needs about Glance tiles. Then choose **Build from AI reply…** and paste the answer. Glance compiles it on your PC, checks it and adds it to your Marketplace, where you review what it can access before installing. If the build fails, one click copies the errors back for the AI to fix. AI-written tiles run with your Windows account's access, like any tile.

Marketplace currently browses bundled tiles and a local catalog. Public submissions and online tile hosting are planned. This repository hosts public documentation and release downloads; application implementation is maintained separately.

## Screenshots

The images below show synthetic test data from version 1.0.0.

![Glance Platform manager](images/v1.0.0/manager.png)

![Finance tile](images/v1.0.0/finance.png)
![Usage tile](images/v1.0.0/usage.png)
![Plex tile](images/v1.0.0/plex.png)

![Create with AI](images/v1.0.0/create.png)
![Building a tile from an AI reply](images/v1.0.0/ai-build.png)