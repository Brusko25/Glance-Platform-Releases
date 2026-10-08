# Glance Platform

Glance puts independent, movable desktop tiles under one manager. Glance Platform 1.4 includes Finance, LLM Usage, Plex, Investments, Weather, Clock and Notes, with shared options, styles and right-click menus.

## Start

Windows 10/11 with .NET Framework 4.8 is required. Download **Glance-Platform-1.4.1-Setup.exe** from the release page and run it. Setup installs for your Windows account and offers a desktop shortcut. Glance appears in Windows **Installed apps / Add or remove programs**. Uninstall removes program files and shortcuts while keeping saved tile data.

For a portable copy, download the Windows ZIP, extract the entire folder, and run Start Glance.cmd. Keep Glance.exe, Glance.TileSdk.dll and the other files together. The included CPU sensor component requires Windows administrator permission. Setup installs or updates it only when needed; if you decline that prompt, Glance still installs, and you can add CPU temperature later with Preferences → Repair CPU temperature. Portable copies request permission on their first normal launch.

Open Glance from the Start menu or its desktop shortcut. If another app starts Glance inside its own private copy of AppData (some developer tools do), Glance says so and doesn't open, so it never works on a separate copy of your tiles.

Try Glance.cmd opens a separate sample workspace. Its Finance, Usage and Plex tiles use synthetic data. Your normal workspace is separate.

## Add and manage tiles

Browse Marketplace to install a bundled tile or import a .glancetile file. Enable installed tiles in My tiles. Marketplace currently uses bundled packages and a local catalog; public hosting and automatic internet tile downloads are planned.

Settings opens the tile's options window, with its own content controls followed by shared Style and Desktop tabs. The more menu provides Tile setup, including live or sample data mode where supported. Changing this mode restarts the tile.

Drag a tile to move it. Right-click for lock, pin, refresh and options. Finance supports multiple chart windows in one tile package. Usage and Plex fit their contents without host title bars.

Scale tiles from 75% to 200% in their options: Finance → Layout → Scale each tile (or right-click a chart → Tile actions → Tile scale); Usage → Display; Plex → Playback → On your widget, then Save options. Clock, Notes, Investments and Weather have their Tile scale slider under Desktop. Each setting is saved independently.

Minimize or close the manager to leave tiles running beside the clock in the system tray. Double-click the tray icon to restore the manager. Choose Quit Glance from the tray to stop all tiles.

## Connect data

- Finance retains charts, portfolio records, local calendar events, saved setups and its original appearance controls.
- LLM Usage offers the original account connection options. Connect only the providers you want. Codex uses a persistent helper; Claude has 5/10/15-minute refresh choices and respects service retry deadlines.
- Plex retains its connection, activity, hardware and optional Tdarr controls. Configure its connections in Settings. The Tdarr section shows CPU and GPU temperatures when available: GPU readings come from Windows, and CPU readings come from the included Glance CPU Sensor service on supported AMD Zen and Intel PCs. No separate monitoring app is required. If setup was cancelled, use Preferences → Repair CPU temperature. Temperatures show Celsius to the left of Fahrenheit; unavailable readings stay hidden. Avoid giving two running Glance Plex instances control over the same Tdarr work.
- Investments combines Webull balances, holdings and reported Open P/L with Voya retirement balances. Connect Webull using your own approved US API access. Enter Voya manually or use your own Plaid Investments account to link a supported plan in the Voya tab. Plaid availability, eligibility and charges depend on your account and institution. Credentials are encrypted locally; failed syncs retain labeled saved values.
- Weather supports city or postal-code search worldwide, current conditions and a 10-day forecast. Choose the matching location and your preferred units in its options. It uses Open-Meteo without an API key.

Fresh installations have no accounts or personal data. Tile data is stored locally under %LOCALAPPDATA%\Glance\Platform\data. The sample workspace uses PlatformTryout. Removing a tile retains its private data for recovery.

## Update and back up

Open **Preferences → Platform updates → Check for updates**. If a newer stable release is available, choose **Install and restart**. Glance downloads from its public GitHub release, verifies SHA-256 checksums and program versions, waits for tiles to finish cleanup, and restarts with your original workspace. Installed copies use the installer; portable copies update in place with a backup for rollback. Existing Glance desktop shortcut icons refresh, and custom workspace arguments are preserved. Updates are started by you; Glance does not silently install a new Platform version.

If any tile cannot confirm cleanup, the update stops and its recovery files are kept. Update logs and portable program backups are under the workspace's updates folder. Update folders older than two weeks are removed when Glance starts. Quit any other workspace using the same program folder before updating. Back up %LOCALAPPDATA%\Glance\Platform before making major changes.

Use **My tiles → Update all installed tiles** to update every installed tile with a newer bundled or local catalog package. Enabled tiles restart after cleanup; disabled tiles stay off. Settings, placement and private data are preserved. A failed tile update does not prevent other tiles from updating. Add a creator's newer .glancetile through **Marketplace → Add to catalog**, then run Update all. Online tile hosting remains future work. Platform upgrades apply newer bundled tiles on restart when each tile's automatic-update preference is enabled; Update all installed tiles also lets you apply them manually.

## Create tiles

To make a tile without writing code, use **Create tiles → Create with AI**: describe what you want, choose **Copy AI prompt**, and paste it into any AI chat. When the AI replies, choose **Build from AI reply…** and paste the reply. Glance compiles it, adds it to your Marketplace, and lets you review what it can access before installing. If the build fails, copy the fix request back to the AI and try again. AI-written tiles run with your Windows account's access, like any tile.

Open Create tiles in the manager, or extract creator-kit.zip. The kit contains the SDK, a starter project, Clock/Notes examples and the creator guide. Native tiles run with your Windows user's permissions; install packages from creators you trust.

## Known limits

Glance's installer and portable app are unsigned. Online marketplace hosting and publisher verification are still planned. Simulated tests cover Tdarr recovery; this release was not verified by controlling a live encoding queue or rebooting Windows.
CPU support installs as Glance CPU Sensor in Windows Installed apps, separately from the per-user Platform app. Its elevated service runs from Program Files and only shares CPU temperature with local readers. Uninstall Glance CPU Sensor there if no longer needed; its uninstaller preserves the shared PawnIO driver for other programs. Unsupported sensors remain unavailable; no Windows security setting needs to be disabled.


## A shared look for your tiles

Right-click a tile and choose **Options…**, then **Style**, or choose **Style…** directly from its menu. **Compact** uses dense rows, a flat surface and small headings. **Classic** uses the rounded Glance presentation and roomier details. Both keep your information available.

Choose the background, corner shape, border style, colour and thickness. The preview changes first; **Apply to this tile** saves only this tile, and **Apply to all tiles** gives every installed tile the same appearance, including tiles currently turned off. The Style tab says a style was applied only after Glance has saved it, and tells you if it couldn't. Applying a style leaves accounts, notes, locations and desktop positions unchanged. You can customize a tile independently afterward.

Every bundled tile uses Finance-style options with a branded header and horizontal tabs. Its own content controls come first, followed by **Style** and **Desktop**. Desktop controls save immediately. Finance keeps chart sizes and arrangements under **Layout**, Usage keeps provider display choices under **Display**, and Plex keeps playback-specific display controls with playback.

The right-click menu follows the same order across tiles. Finance's chart controls and Notes' text-editing commands are under **Tile actions**.
