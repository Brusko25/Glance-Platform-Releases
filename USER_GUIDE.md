# Glance Platform

Glance puts independent, movable desktop tiles under one manager. This first public preview includes Finance, LLM Usage and Plex, plus Clock and Notes examples.

## Start

Windows 10/11 with .NET Framework 4.8 is required. Download the Windows ZIP from the release page, extract the entire folder, then run Start Glance.cmd. Keep Glance.exe, Glance.TileSdk.dll and the other files together. No administrator installation is required.

Try Glance.cmd opens a separate sample workspace. Its Finance, Usage and Plex tiles use synthetic data. Your normal workspace is separate.

## Add and manage tiles

Browse Marketplace to install a bundled tile or import a .glancetile file. Enable installed tiles in My tiles. Marketplace currently uses bundled packages and a local catalog; public hosting and automatic internet tile downloads are planned.

Settings opens the tile's original options window. The more menu provides Tile setup, including live or sample data mode. Changing this mode restarts the tile.

Drag a tile to move it. Right-click for lock, pin, refresh and options. Finance supports multiple chart windows in one tile package. Usage and Plex fit their contents without host title bars.

Minimize or close the manager to leave tiles running beside the clock in the system tray. Double-click the tray icon to restore the manager. Choose Quit Glance from the tray to stop all tiles.

## Connect data

- Finance retains charts, portfolio records, local calendar events, saved setups and its original appearance controls.
- LLM Usage offers the original account connection options. Connect only the providers you want. Codex uses a persistent helper; Claude has 5/10/15-minute refresh choices and respects service retry deadlines.
- Plex retains its connection, activity, hardware and optional Tdarr controls. Configure its connections in Settings. Avoid giving two running Glance Plex instances control over the same Tdarr work.

Fresh installations have no accounts or personal data. Tile data is stored locally under %LOCALAPPDATA%\Glance\Platform\data. The sample workspace uses PlatformTryout. Removing a tile retains its private data for recovery.

## Update and back up

Quit Glance before replacing the portable program folder. Extract a new release to a new folder and run its Start Glance.cmd; it uses the same normal workspace. Back up %LOCALAPPDATA%\Glance\Platform before making major changes.

A newer tile package can be added to the local catalog and installed from Marketplace. Settings, placement and private data are preserved. The first preview does not include a host installer or automatic online updates.

## Create tiles

Open Create tiles in the manager, or extract creator-kit.zip. The kit contains the SDK, a starter project, Clock/Notes examples and the creator guide. Native tiles run with your Windows user's permissions; install packages from creators you trust.

## Preview limits

This is an unsigned portable preview. Online marketplace hosting, publisher verification and a Windows installer are still planned. Simulated tests cover Tdarr recovery; this release was not verified by controlling a live encoding queue or rebooting Windows.