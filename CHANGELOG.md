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