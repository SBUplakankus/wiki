---
icon: lucide/monitor
---

# BigScreen Mode

BigScreen is the fullscreen, controller-friendly launcher for TV / couch use. It is a separate application project (`XeniaManager.BigScreen`) sharing the same core library, library data (`Config/games.json`), and emulator installs as the desktop app.

!!! info "Screenshot needed"
    **File:** `assets/images/bigscreen-mode.png`
    **Capture:** BigScreen home screen with game grid focused, fullscreen.
    **Replace with:** `![BigScreen mode](assets/images/bigscreen-mode.png)`

---

## Launching and Startup Options

- **From the desktop app**: look for the BigScreen launch action (toolbar/page action depending on version).
- **Start in Big Screen** (`General → Start in Big Screen`, default off): boots straight into BigScreen instead of the desktop window. See [Manager Settings](manager-settings.md#general). Turn this on for a dedicated emulation box; keep it off while you are still configuring things, since settings editing is faster in the desktop UI.
- Exiting BigScreen returns you to the desktop (or exits entirely, depending on how it was launched).

## What You Can Do There

- Browse the same Library (artwork grid, search/sort where exposed).
- Launch games with their assigned variants - per-game settings, content, and patches apply exactly as in desktop mode.
- Basic management (content/patch/settings access depends on version - the desktop app remains the full-featured surface).

Prefer the desktop app for: first-time Xenia installation, patch editing, config tuning, profile/save surgery, and Steam shortcut creation. Use BigScreen for: launching and playing.

> For how the BigScreen screens work internally (Dashboard, Library, navigation, modal stack), see the [BigScreen deep dive](../big-screen/overview.md).

## Tips

- Set up everything in desktop mode first (install emulators, scan library, verify one game boots), then switch to BigScreen for daily use.
- If BigScreen shows an empty library, the desktop app would too - rescan in desktop mode ([Library](library.md#scanning-and-adding-games)); both read the same `games.json`.
- Dashboard preferences persist to `Config/dashboard-settings.json` next to the other config files.

---

## Troubleshooting

- **BigScreen starts but games fail to launch** - diagnose in desktop mode where error output and logs are visible ([Troubleshooting](../help/troubleshooting.md#logs)), then return to BigScreen.
- **Controller does not navigate BigScreen** - confirm Xenia's `gamecontrollerdb.txt` is present and your controller works in the desktop app first; BigScreen relies on the same SDL mapping pipeline.
