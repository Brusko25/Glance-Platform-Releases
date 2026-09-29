# Glance Platform 1.2.0

- **Plex tile 1.2.0 shows CPU and GPU temperatures** beside the CPU and GPU percentages in the Tdarr section. The GPU temperature is the one Windows itself reports, the same value Task Manager shows (graphics drivers from 2018 on). Windows has no built-in CPU temperature, so the CPU temperature appears only while HWiNFO (with Shared Memory Support turned on) or LibreHardwareMonitor is running. Glance installs no drivers. Temperatures use °F when Windows is set to a non-metric region, otherwise °C. When no source reports a temperature, nothing is shown.
- Uninstalling or updating no longer fails with "Glance could not finish closing" when a Glance process is exiting at the moment it is checked.
- Folders left by Platform updates (the download, extracted copies and the backup of replaced files) are removed after two weeks.

# Glance Platform 1.1.1

- **Start with Windows follows your workspace.** Turning Start with Windows on or off now works from any copy of Glance that opens the same workspace, such as the installed app after using a portable copy. If the startup entry points to a Glance that was moved or removed, Glance points it at the copy you are running the next time it opens.
- **LLM Usage tile 1.1.3:** closing its options window no longer disposes the tile's icon, which could log "Cannot access a disposed object: Icon" and break the tile's window icon until restart. The options, provider and About windows each use their own copy of the usage-bars icon.
- LLM Usage tile 1.1.2 restores the existing Codex desktop sign-in, including saved desktop connections. Account setup offers both desktop and separate browser sign-in. The desktop helper must have a valid OpenAI signature; persistent polling, clean shutdown, Claude timing and browser sign-in remain in place. The obsolete local retirement delay is cleared without clearing service cooldowns.
- Finance and LLM Usage tile packages 1.1.1 use their approved trend-arrow and usage-bars artwork in options headers and window icons. The Platform G stays with the manager. The maintained tile sources and their provenance hashes are updated; standalone repositories are unchanged.

# Glance Platform 1.1.0

- **Platform updates:** Preferences checks the latest stable GitHub release. Install and restart downloads and verifies the release, waits for clean tile shutdown, and keeps the current workspace. Portable updates retain a backup and roll back file replacement failures; installed copies use setup.
- **Update all installed tiles:** My tiles updates installed packages from the bundled tiles and local catalog. Settings, data, placement and enabled state are retained. Failures are reported per tile, and cancelling restores any tile already stopped cleanly. Hosted tile catalogs remain future work.
- **Windows installer:** per-user setup, Start menu entry, optional desktop shortcut, and Windows Installed apps / Add or remove programs support. Uninstall preserves private tile data. Existing Glance desktop shortcut icons refresh during updates, preserving custom workspace arguments.
- All bundled packages are now 1.1.0. Finance, Usage and Plex keep their maintained source based on the final standalone releases (2.6.6, 2.2.1 and 2.3.0 respectively). No new account or service behavior is introduced.

# Glance Platform 1.0.0

The first full release. It includes everything from the 0.2 previews, Create with AI from 0.2.9, and a new icon set. The tiles are still based on Finance 2.6.6, LLM Usage 2.2.1 and Plex 2.3.0; their packages are version 1.0.0, so Marketplace offers them as updates to 0.2.x packages. Existing workspaces, settings, tile data and layouts are kept.

- **New icons.** The black, mint and lavender icon set now appears beside tile names in Marketplace, My tiles, the desktop sidebar and tile details. The Platform G is used for the manager header, Glance.exe, the tray and shortcuts. Tiles without built-in artwork, including the ones you create, keep their initial.
- **Plex tile icon.** The floating Plex tile's header and its options window show the Plex playback icon instead of the Platform G.
- The portable folder name now starts with Glance-Platform-1.0.0 instead of "preview", and the folder includes Glance.ico for desktop shortcuts.

# Glance tiles 0.2.9

Create tiles without writing code. The tiles are unchanged: Finance 2.6.6, LLM Usage 2.2.1 and Plex 2.3.0; their packages are version 0.2.9.

- **Create with AI.** Create tiles has a new section: describe the tile you want and choose **Copy AI prompt**, then paste the prompt into any AI chat. The prompt includes the whole tile SDK, the manifest rules, the C# 5 / .NET Framework 4.8 limits, a working example, safety rules and a reply format Glance can read. Choose **Build from AI reply…**, paste the answer, and Glance compiles it on this PC, checks that it can start, packages it and adds it to your Marketplace for review and install. If the build fails, **Copy fix request for the AI** copies the errors back in one paste. **Preview in a test workspace** runs the new tile separately first.
- Glance.Tools.exe has a new `--check-entry <folder>` command that verifies a tile's entry class without running it.

# Glance tiles 0.2.8

The Plex tile now includes Glance Plex 2.3.0 with a simple Tdarr rule: while anyone is watching Plex, playing or paused, the tile pauses every Tdarr node, including nodes that connect during playback, and resumes them once no one has watched for the resume delay (5 minutes by default). Node selection and the older stream filters are gone, so a saved selection or filter can no longer leave nodes running during a stream. Automatic pausing is on by default and updating turns it on once; you can turn it off in the Plex tile's options. The tiles also include Finance 2.6.6 and LLM Usage 2.2.1, which only change the standalone apps' icons. Existing connections, preferences, history and layouts are retained.

# Glance tiles 0.2.7

Manager improvements. The tiles still run Finance 2.6.5, LLM Usage 2.2.0 and Plex 2.2.3; their packages are version 0.2.7.

- Fix the Desktop map showing only one Finance chart. It now tracks every visible chart, including movement, opening, closing and show/hide changes.
- Remove the repeated page headings, Marketplace introduction and My tiles introductory panel so each page starts with its controls and content.
- Label the Marketplace search field "Search tiles".
- Show Marketplace tiles as compact full-width rows with their name, version and install/update state. Click a row or its name to see its description, author and declared access; installed tiles open details without reinstalling.

# Glance tiles 0.2.6

The Usage tile now includes Glance LLM Usage 2.2.0, which retires the option that read Codex through the Codex app's own codex.exe. Codex is tracked through Sign in with ChatGPT and its pinned, verified helper. If a Usage tile still used the old option, its Codex row explains how to switch until you sign in with ChatGPT or stop Codex monitoring; nothing else changes. "Existing desktop connections…" is now "Claude desktop sign-in…". Finance (2.6.5) and Plex (2.2.3) are unchanged.

# Glance tiles 0.2.5

The Usage tile now includes Glance LLM Usage 2.1.3. Claude checks keep the sign-in token in memory instead of decrypting Claude's saved sign-in every time, which cuts calls to Windows' security service (lsass) to about one per token. The token is read again when Claude renews it, when you switch accounts in Claude, when it has five minutes or less left, or if Claude rejects it. Finance (2.6.5) and Plex (2.2.3) are unchanged. Existing connections, preferences, history and layouts are retained.

# Glance tiles 0.2.4

Tiles now include Glance LLM Usage 2.1.2, Glance Finance 2.6.5 and Glance Plex 2.2.3. Existing connections, preferences, history and layouts are retained.

- Usage: Claude checks every 5 minutes by default and shows STALE only when its reading is actually old, not after one rate-limited check. Codex checks every minute by default (1, 2, 5 or 10 minutes). Checks pause while Windows is locked or asleep.
- Finance: failed price refreshes back off from 30 seconds to 5 minutes, the control panel refreshes only while it's on screen, refreshes pause while Windows is locked or asleep, fonts are shared, Ctrl+4 to Ctrl+0 display correctly, and About names the real price sources.
- Plex: if Plex can't be reached while Tdarr is paused, Tdarr resumes after 10 minutes (30 minutes, 1 hour or Never in Plex options) with a notification. Plex tokens and Tdarr API keys are never sent over plain http outside the home network. A disconnected paused node shows that Glance is waiting for it, a failing encoder guard is retried with growing delays, and viewing history shows its dates correctly.
- Glance can always quit, even when a running tile's package has become unreadable.
- Marketplace and update checks read each package's manifest directly instead of unpacking every package. Installing still fully validates the package.
- Leftovers in the workspace's staging folder are removed after two weeks.
- The tile build fails if an adaptation no longer matches the original app's source, instead of silently skipping it.

# Glance tiles 0.2.3

- Updates the Plex tile to Glance Plex 2.2.2. Widget resources and the owned icon are disposed once, and cleanup tolerates an already-cleared tray menu.
- Adds a hosted Plex regression that repeats disposal after normal and system shutdown cleanup.
- Includes the existing Finance 2.6.4 and Usage 2.1.1 sources. Tile settings, connections, history and layouts are retained.

# Glance tiles 0.2.2

Includes the complete source updates from Finance 2.6.4, LLM Usage 2.1.1 and Plex 2.2.1.

- Finance preserves local transaction/event dates across restarts, recovers unreadable workspaces safely, confirms record removal, and keeps portfolio selections during quote refreshes. Recovery details are available in its original Settings screen.
- Usage reuses a persistent Codex helper, closes it gracefully, and waits for helper cleanup before the tile worker exits. Sign-in changes release idle helper sessions. Existing Claude refresh preferences and cached readings are preserved.
- Plex uses durable settings/history/lease writes, retries transient Tdarr guard file failures, retires idle guards, and saves activity progress on exit. Windows shutdown invokes bounded cleanup without cancelling shutdown; unresolved leases remain available for recovery.
- The Plex adapter serializes simultaneous saves within its worker to avoid a file-replacement race found by Windows CI.
- Each tile package includes UPSTREAM.json identifying its source version and SHA-256 file hashes.

Validation uses the platform suite, the upstream offline Finance suite, simulated Codex helpers, Claude polling fixtures, and the upstream simulated Plex/Tdarr suite. Live Tdarr control and an actual Windows restart were not performed.

# Glance tiles 0.2.1

- Settings opens the tile's original options directly. Tile setup remains in the more menu.
- Claude polls every five minutes by default, with 5/10/15-minute choices in Accounts.
- Successful Claude readings and polling deadlines survive restarts. Refresh cannot bypass the chosen interval or a service retry deadline.
- Removes the redundant My tiles page banner.
- Tab changes keep the navigation and surrounding window in place; only page content is repainted.
- Minimize sends Glance to its tray icon beside the clock. Double-click restores the manager.

# Glance tiles 0.2.0

- Restores the original Finance control center, multiple charts, portfolio, saved setups, appearance and shortcuts.
- Restores Usage Desktop, Appearance, Updates and Support controls.
- Connects Usage and Plex pinning, lock, snap, opacity and monitor controls to the real hosted windows.
- Glance handles startup, shortcuts and local package update checks.
- Updates preserve tile data and preferences. Online tile hosting is planned.
- Native desktop tiles remain borderless and movable.

Provider connections, market data, Plex playback and optional Tdarr controls use the original implementations. Settings stay on this PC.
