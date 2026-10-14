# Unreleased

# Glance Platform 1.4.13

- Included package versions: Finance 1.4.4, Usage 1.4.4, Plex 1.4.5, Investments 1.1.18, Weather 1.1.4, Clock and Notes 1.4.1, and Liquid Icons 1.2.0. The installer and portable ZIP include all eight tiles.

- Liquid Icons 1.2.0 adds a Glass material with its own options page. Five presets (Clear, Frosted, Smoked, Black and Neon) are starting points; tint (clear to fully black, in any color), frost, edge shine, gloss, edge depth, edge thickness, shadow, an optional colored glow and the light direction can each be adjusted with a live preview. Joined icons stay one piece of glass. Glass never reads or blurs the wallpaper, so animated wallpapers keep running underneath. Moving icons draw at half resolution and sharpen when they settle. Existing settings keep the Liquid look. Dropped icons now jiggle: when one lands next to others, its liquid squashes and stretches for about a second and the joined pool ripples in answer; a drop on its own gets a small settle. Drop Jiggle on Shape And Motion sets the strength or turns it off, and clicking the preview plays it.

- Platform 1.4.13: Setup closes a running Glance the same graceful way uninstall does before replacing files, so tiles that were on stay on after installing over a running Glance. Snapped-tile merging no longer wakes every tile 20 times a second: a tile only watches its neighbours when its own frame shows merging (rounded corners or a border), checks four times a second once the desktop is quiet, and speeds up for a few seconds after a tile moves. Square, borderless tiles never poll, and neighbours still merge against them.

- Liquid Icons 1.1.3 reads desktop icon positions about once a second when the desktop is quiet, every 300 ms for a few seconds after a change or desktop click, and not at all while hidden, instead of every 300 ms forever. A drawing failure, such as Explorer being busy right after sign-in, is retried automatically after 5, 10, 20, 40 and 60 seconds instead of staying blank until Refresh. Only the desktop's own windows are used, so an old-style Open/Save dialog no longer clears the backgrounds while it is open.

- Investments 1.1.18 stops showing last year's Voya YTD return and dollar gain after January 1; they wait for this year's first valuation. Browser, manual and Plaid Voya values older than a week show "As Of" with their date, since they are added to live Webull values. Background refreshes preserve the unclear transaction selected for review; if it disappears, the selection stays empty until you choose another. A typed starting gain clears when its account, balance or valuation date changes, and Save Starting Point also refuses a balance changed since the last refresh. Saved browser data that can't be opened can now be moved aside with Start over, and starting points for renamed plans are dropped. Starting the tile with Browser Import on refreshes the extension and helper files, so Reload in the browser picks up the current helper.

- Liquid Icons 1.1.2 prevents unrelated backgrounds from flashing when desktop icons are deleted. Interrupted Explorer scans retain the last complete frame, and stationary backgrounds are matched by position before animation IDs so reassigned IDs cannot pull them across the desktop. Real empty/hidden desktops still clear normally; direct dragging is preserved.

- Platform 1.4.12 brings tile Options to the front when opened from the sidebar, Settings buttons or menus. Platform grants foreground permission to the selected tile before sending the request, and existing minimized Options windows are restored, including modal dialogs. Background refreshes do not request focus.

- Liquid Icons 1.1.1 makes the droplet rim visible on black backgrounds and at lower strengths. A brighter highlight sits inside the edge, with reflected light defining the opposite side instead of relying on an invisible black shadow. Rim 0 keeps the flat appearance.

- Liquid Icons 1.1.0 adds custom colors and swatches, crisp-to-soft edges, an optional raised droplet rim, Rounded/Pill/Square shapes, independent background width and height, and wider padding and join controls. Two options pages preview changes before saving. The rim lights only the merged outside edge; classic black remains the default. GPU composition, direct dragging and idle section caching remain in use, with color preserved by the compatible renderer too.

- Platform 1.4.11 clears old rounded card borders while resizing the manager, including the My Tiles summary bar. Shared cards now repaint their full surface on size changes. Verified with repeated horizontal and vertical resize paint checks and dark/light synthetic previews.

- Liquid Icons 1.0.5 follows dragged icons directly and uses GPU composition with full transparency, updating changed sections together in one frame. Motion follows the Windows compositor clock instead of a coarse window timer, and a busy UI skips obsolete frames. Selected groups follow together; a fresh Windows snapshot confirms the final snapped position with a brief settle. Explorer position polling pauses during dragging. Settle motion is now 50–250 ms. Unsupported or reset graphics devices fall back to compatible desktop drawing. The synthetic 110-icon benchmark reduced moving-frame work from about 17 ms in the local 1.0.3 build to about 4 ms; real desktop checks cover transparency, removal, focus and lifecycle.

- Liquid Icons 1.0.2 fixes invisible desktop backgrounds on Windows 11 builds that accept per-pixel layered child windows but never display them. Redirected drawing with separate opacity regions preserves soft edges and transparency. Startup prepares the shell's background layer, and drawing errors remain visible until retried. Verified against actual desktop pixels, including partial opacity and removal.

- Liquid Icons 1.0.0 is a separate optional tile with black liquid backgrounds behind existing desktop icons. Nearby pools join with rounded inward curves, and rearranged icons transition smoothly. Appearance options control padding, roundness, connection reach, opacity and motion. Windows keeps handling icons normally; disabling or hiding the tile removes its surface. Requires the layered icon view in modern Windows 11. No icon names, file contents or positions are saved.

- Investments 1.1.17 adds an estimated total return marked ≈, calculated from combined Voya dollar gains and Webull open P/L divided by the matching invested amounts. IAP and cash are excluded from both sides of this calculation. The tooltip explains that it mixes return periods and ignores contribution timing. Missing or pending investment data keeps the estimate unavailable.

- Investments 1.1.16 adds an aligned percentage column for invested holdings and provider totals, and removes routine Updated / As Of lines for a shorter tile. Webull percentages use unrealized gain or loss divided by the holding cost; its subtotal is weighted by invested cost. Voya can show the reported YTD return of its single invested plan. Cash and IAP without return data have no percentage. Unavailable data and a total mixing different return measures show a dash. Connection errors retain a visible status row.

- Investments 1.1.15 puts each Voya plan's percentage on the same row as its name, dollar gain and balance, removing the extra return line for a shorter tile. The tooltip identifies the percentage as YTD.

- Investments 1.1.14 places each Voya plan's dollar gain on the same row as its name and balance, aligned with Webull's gains. The YTD percentage stays below the plan name.

- Investments 1.1.13 aligns Voya dollar gains in the shared Gain / P/L column beside the YTD percentage, adds a bold Voya gain subtotal and a combined top total with Webull, and shortens the tile's plan labels to IAP and Def Comp. Totals include only Voya plans with gain tracking; pending tracked gains or missing Webull P/L keep the combined figure unavailable. The tooltip explains the mixed YTD and unrealized measures.

- Investments 1.1.12 / browser helper 1.0.6 fixes Voya's transaction-filter detection by reading the selected caption inside each v-select component's open shadow root and checking its reflected value. Unselected option labels cannot satisfy the filter check. Verified against an offline saved transaction page; reload the extension after updating.

- Investments 1.1.11 / browser helper 1.0.5 reads selected transaction filters displayed in readonly text inputs or input buttons. Custom dropdown values are not exposed through innerText. Hidden, password and editable input fields are excluded. Reload the extension after updating; the owner is verifying the live import.

- Investments 1.1.10 / browser helper 1.0.4 tolerates whitespace in rendered transaction headings, filter labels and currency values. A failed page read now names the missing filter, balance/date, result count or table detail. The popup shows its version and updates its status while open. Live Voya transaction-page compatibility is still being verified with the owner.

- Investments 1.1.9 / browser helper 1.0.3 accepts a Completed Transactions report with explicitly zero results, even when Voya omits the table or shows an empty-state row. Applied dates, All Activity / All Funds and the matching ending balance are still required. Reload the extension after updating.

- Investments 1.1.8 shows calculated Voya YTD dollar gains beside the reported percentage. Browser helper 1.0.2 reads complete, unfiltered Completed Transactions on my.voya.com and updates gains against an encrypted starting balance and gain. Outside deposits and withdrawals are excluded, internal transfers must balance, and unclear activity is reviewed in Browser Voya options. Partial history, mismatched valuations and a new calendar year show gains pending instead of stale dollar amounts. Reload the extension after updating.

- Investments 1.1.7 aligns all balances in one value column, uses purple provider headings and bold totals, and removes repeated plan dates for a shorter tile. Browser Voya can import an account Info page's reported YTD return when its name, balance and date match the dashboard. Returns are labeled as percentages, kept separate from Webull's dollar Open P/L, and cleared when the dashboard valuation changes. Reload the Glance Voya extension after this update.
- Investments 1.1.6 adds opt-in Browser Voya for Opera GX. Signing into Voya and viewing the dashboard imports its total, individual account balances and their dates through a local browser helper. Saved browser values remain available after sign-out; Webull keys, Plaid data and manual Voya entries stay separate. Browser import pauses Plaid refresh until switched off. Requires loading the supplied extension once in Opera GX.
- Desktop action buttons now share one size and consistent column spacing across both rows.
- Fixed gaps where inward merge curves meet straight tile borders. Each tile paints its own part of the curve, so a neighboring window cannot cover the join.
- Unlock All Tiles now clears the individual locks on every Finance chart, including hidden charts and a Finance tile that is off. Later per-chart choices survive unrelated desktop changes and restarts. Finance 1.4.4.
- Snapped tiles merge their touching borders and corners over a visible one-second transition, leaving an outline around the outside. Inward corners use the same curve as the outside corners, including partial and L-shaped joins. Partial joins preserve exposed edges; separating or hiding a tile restores its own frame. Style → Merge Snapped Tiles can be turned off or applied to all tiles. Style adds Merge Animation: Follow Windows, On (1 Second), or Off. On enables the effect specifically in Glance when Windows animations are disabled; high contrast skips animation. Includes Finance 1.4.3, Usage 1.4.4, Plex 1.4.5, Weather 1.1.4, Investments 1.1.5, and Clock and Notes 1.4.1.
- Platform's Desktop tab adds Lock All Tiles and Unlock All Tiles, including every Finance chart and tiles that are currently off. Locking preserves positions and keeps tiles updating; the saved choice survives restarting Glance.
- Options windows repaint their old card edges during resizing, fixing repeated outlines and text trails across the tile family. Buffered page surfaces and batched layout reduce flicker; Finance reuses its quote, news and calendar controls while resizing instead of rebuilding them for every pixel. The darker cards, rounded corners, saved settings and connections are unchanged. Includes Finance 1.4.2, Usage 1.4.3 and Plex 1.4.4; existing Weather and Investments packages receive the shared repaint fix from Platform.

# Glance Platform 1.4.4

- All tile options use the darker Codex card color, including their leading cards. Usage keeps the same rounded corners and outlines as the other tiles when pages refresh or resize. Section titles and tabs capitalize every word, including Live Usage, Provider Websites and Find Your Local Weather. Finance 1.4.1, Usage 1.4.2, Plex 1.4.3, Weather 1.1.3 and Investments 1.1.4 preserve existing settings and connections.
- Included package versions: Finance 1.4.1, Usage 1.4.2, Plex 1.4.3, Weather 1.1.3, Investments 1.1.4, and Clock and Notes 1.4.0. The installer and portable ZIP include all seven tiles.

# Glance Platform 1.4.2

- Weather and Investments 1.1.2 now follow Finance's options layout: rounded section cards, consistent typography and spacing, aligned fields and a fixed footer. Weather groups location search and forecast preferences; Investments groups Webull, Voya, verification and holdings. Pages fit narrow windows without horizontal scrolling, and account connections and saved values are preserved.
- Weather and Investments have matching black, lavender and mint icons in Platform and their options. Investments uses a dollar sign behind rising bars.
- All seven tile options use the Platform header proportions, transparent icon edges and dark Windows title bars. Platform and tile options use native dark scrollbars and matching input borders, while retaining native scrolling and keyboard behavior. Light surfaces and Windows high contrast keep native decoration.
- Scrollbars keep one consistent appearance during scrolling and dragging. Removed a second drawing layer that was alternating with Windows' own scrollbar renderer.
- Installed tile IDs and private data are unchanged; the updated Weather and Investments packages retain existing settings and credentials.
- Included package versions: Finance, Usage, Clock and Notes 1.4.0; Plex 1.4.1; Investments and Weather 1.1.2. The shared options appearance is supplied by Platform 1.4.2.

# Glance Platform 1.4.1

- **Updating Glance no longer asks for administrator permission every time.** Setup only installs the CPU sensor when it is missing or out of date. If you decline the Windows prompt, or your account isn't an administrator, Glance still installs or updates; CPU temperature can be added later with Preferences → Repair CPU temperature. The sensor and its driver are no longer installed on processors they can't read, and the Glance window no longer freezes while CPU temperature is being set up.
- **Tiles stay on after Windows restarts.** Tiles that were running when Windows shut down start again at your next sign-in. Glance could previously save them as turned off while Windows was ending the session.
- **Marketplace stays usable when a tile's files are damaged.** A missing, oversized or damaged manifest, a missing entry DLL, or valid JSON with damaged values no longer hides the catalog. The affected tile offers Repair, which restores its files from the catalog package and keeps its settings, saved data and position. Installing over a leftover package folder now works instead of saying the tile is already installed; the old folder is kept.
- **Safer updates and repairs.** If an install, update or repair fails and Glance can't fully undo it, the message says what happened and where the earlier files are kept. Staging cleanup keeps a replaced package while its tile has no readable package. A broken tile no longer hides update notices for the others, and a read-only log file can no longer stop Glance from starting.
- **One Glance workspace.** Glance won't open its workspace, or install a Platform update, when it is started from inside an app that Windows gives a private copy of AppData, such as the Codex desktop app. Glance checks where its files really are, so this works even when Windows doesn't report that the app started it. Start Glance from the Start menu or its shortcut.
- **Style and menus:** Style reports "applied" only after Glance confirms it saved that change, and says so if it couldn't, including when copying a tile's current style to all tiles. A tile's own right-click actions (such as Notes editing) no longer linger in later menus. Dragging tiles with snapping is smoother.
- **Weather 1.1.1:** Cancel and Escape close Weather options, and a newly chosen location loads straight away.
- **Investments 1.1.1:** if saved investments can't be opened on this PC (for example after a Windows account change), Options offers Start over. The unreadable file is moved aside in the tile's data folder, never deleted. Fields are locked while an action runs.
- **Plex 1.4.1:** the compact layout keeps its footer and Tdarr row in place when Plex is slow to answer.
- Included package versions: Finance, Usage, Clock and Notes 1.4.0; Plex 1.4.1; Investments and Weather 1.1.1.

# Glance Platform 1.4.0

- **A shared tile family:** every bundled tile now uses Finance-style options chrome, horizontal tabs, a common Style tab and the same Desktop controls. Provider connections, portfolios, chart layouts, notes and location settings remain local and separate from style.
- **Compact or Classic:** select the flat, data-first look or the original rounded Glance look for Finance, LLM Usage, Plex, Investments, Weather, Clock and Notes. Compact Usage omits decorative bars and shortens rows; compact Plex removes routine checked-at footer text while retaining errors and overflow notices. Details remain available on hover.
- **Make the surface yours:** choose theme, black, charcoal, navy, paper or a custom background; square, soft or rounded corners; no border, subtle outline, accent or custom border colour; and 1–4 pixel borders. Text and semantic status colours adapt to light backgrounds.
- **Apply to all tiles:** the Style tab previews changes before applying to this tile or every installed tile, including disabled tiles. This copies only appearance. Each tile can still be customized independently afterward.
- **One right-click menu:** Options, Style, Refresh, desktop placement controls, Hide, Open Glance and Disable appear in the same order. Finance keeps chart commands under Tile actions; Notes keeps its editing commands there.
- **Weather is maintained with Platform:** the current compact 10-day weather tile, international location search, units and source credits are included in the maintained source and package build. Existing weather tile identity and saved settings are retained.
- Included package versions: Finance, Usage, Plex, Clock and Notes 1.4.0; Investments and Weather 1.1.0. Platform 1.4.0 keeps SDK ABI version 1 and adds optional family UI/style extensions.

- **Investments 1.0.4:** adds optional Voya auto-sync using your own Plaid Investments account. New Voya options open browser approval, preserve and reuse pending connections, support reconnect/disconnect, and check saved balances hourly. Credentials and data are encrypted locally; failed reads keep labeled saved values. Webull and manual Voya entries are preserved. Trial eligibility and Voya plan support depend on Plaid; no paid-plan upgrade or forced Investments Refresh is performed.

- **Investments 1.0.3:** automatically fits the desktop tile to compact rows, removing unused bottom space. Adds signed, color-coded Open P/L beside the Webull total and each position value. Open P/L sums Webull's reported unrealized position gains/losses, excludes cash, and stays unavailable when any position is missing a figure.

- **Investments 1.0.2:** combines Webull cash across accounts into one row and uses Webull's name and total as the holdings heading. Removes the repeated Webull summary and attribution footer. The tile is shorter, with a compact combined total shown once both balances are available; Voya fund details remain in options.

- **Investments 1.0.1:** fixes blank BTC values when Webull omits the crypto position's currency. Crypto can inherit its confirmed USD account currency, and holdings prefer Webull's reported market value. Account totals are unchanged.

- **Investments tile:** combine Webull account balances and holdings with manually maintained Voya retirement investments. Webull uses its official US API with local encrypted credentials, optional two-step verification and adjustable refresh timing. Missing balances remain unavailable; failed syncs retain labeled saved values. Voya includes a balance date and optional fund holdings. API access must be approved by Webull before connecting.

# Glance Platform 1.3.1

- **Celsius alongside Fahrenheit.** Plex shows both CPU and GPU temperatures with Celsius on the left, such as 54°C 129°F, beside the usage percentage. Unavailable readings stay hidden. Included Plex tile version: 1.3.2.
- **Focused publishing checks.** Routine releases verify startup, saved data, updates, package integrity and installation. Broader provider, Tdarr and hardware suites remain available for relevant changes and manual runs.

# Glance Platform 1.3.0

- **CPU temperature without a separate monitoring app.** Setup includes Glance CPU Sensor and the signed PawnIO driver. Approve the Windows administrator prompt during installation; the sensor service then starts with Windows and Plex reads it automatically. Portable copies set up the same component on first normal launch. Supported AMD Zen and Intel digital thermal sensors report temperature; unsupported or blocked sensors stay blank. GPU readings still come from Windows. Temperature units follow your Windows region.
- **Scale each tile from 75% to 200%.** Finance has an independent slider for each chart under Desktop and in its right-click Tile scale menu. LLM Usage has its slider under Appearance; Plex has it under Playback / On your widget. Clock and Notes use their tile settings. Text and contents scale with the tile, and the setting is saved.
- **Platform updates include bundled tile updates.** Newer bundled tiles apply on restart when their automatic-update preference is enabled, preserving settings, placement and private data. Finance, Usage, Clock and Notes are version 1.3.0; Plex is 1.3.1 so it also replaces the earlier manual sensor test package.
- **Simpler release preparation.** One command builds and checks the candidate, then packages those same files. Release tags no longer trigger a redundant build.

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
