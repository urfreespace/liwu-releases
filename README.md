<p align="center">
  <img src="https://liwu.app/app-icon.png" width="96" alt="Liwu icon">
</p>

<h1 align="center">Liwu</h1>
<p align="center"><b>Small tools for your MacBook, right in the menu bar.</b><br>
Charging targets, Sailing, live power, battery health history, Keep Awake, calibration, schedules, notifications, and menu bar organization.</p>

<p align="center">
  <img src="https://liwu.app/screenshots/v2-popovers/hero-popover-2.png" width="330" alt="Liwu 2 Battery tab with power readings, calibration progress, and Keep Awake">
  <img src="https://liwu.app/screenshots/v2-popovers/menu-popover-zones-3.png" width="330" alt="Liwu 2 Menu Bar tab with Hidden, Visible, and Always Hidden icon groups">
</p>

## Choose your version

| Version | Requirements | Download |
|---|---|---|
| **Liwu 2** | Apple Silicon MacBook, **macOS 26.7 or later** | [Latest release](https://github.com/urfreespace/liwu-releases/releases/latest) |
| **Liwu 1 Legacy** | Apple Silicon MacBook, macOS 14 through versions before 26.7 | [Legacy website](https://liwu.app/legacy) · [1.0.8 installer](https://github.com/urfreespace/liwu-releases/releases/download/v1.0.8/Liwu-1.0.8.dmg) |

Liwu 1 is frozen and receives no further feature updates. Do not install it on macOS 26.7 or later.

Liwu 2 is available in English, Simplified Chinese, German, French, Spanish, Brazilian Portuguese, Korean and Japanese. It follows your Mac's language, and you can choose one in General.

## Install Liwu 2

With Homebrew:

```sh
brew install --cask urfreespace/liwu/liwu
```

Or download the DMG from [Releases](https://github.com/urfreespace/liwu-releases/releases/latest), open it, and drag Liwu to Applications.

On first launch, follow the prompts to approve Liwu's background component. Charging control needs this component. Menu bar organization separately requests Accessibility and Screen Recording permissions when you use it to read and move icons.

Releases are signed with a Developer ID certificate and notarized by Apple. Updates are available inside the app.

## What Liwu 2 does

| Feature | What it does | Free | Pro |
|---|---|:---:|:---:|
| Charging targets · 20–100% | Set the level charging stops at. Below 80% needs supported low-target control; otherwise the minimum stays at 80% | ✓ | ✓ |
| Named presets | Save your favorite targets and switch between them | ✓ | ✓ |
| Power in the battery bar | Adapter input and battery charging or discharging power, with details on demand | ✓ | ✓ |
| Menu bar organization | Sort icons into Always Hidden, Hidden, and Visible; show or hide the Hidden group from arrows in the menu bar | ✓ | ✓ |
| Optimized Battery Charging | See when it conflicts with charging management and turn it off from Liwu | ✓ | ✓ |
| Keep Awake · Lid Open | Keep long jobs running, with a timer and a low-battery cutoff | ✓ | ✓ |
| Battery health history | One reading a day of maximum capacity and cycle count, charted over time | ✓ | ✓ |
| Notifications | A warning at a battery level you choose, for the Mac and for accessories that report their level to macOS; also when calibration ends, a plan does not run, or charging control needs attention | ✓ | ✓ |
| Top Up | Temporarily request 100% without losing your regular target | | ✓ |
| Sailing · Charging range | Let the level drop 5–20 percentage points before recharging | | ✓ |
| Battery calibration | A five-step cycle that returns to your regular target | | ✓ |
| Target, Top Up & calibration plans | Schedule targets, Top Up or calibration cycles, with skip-once and catch-up | | ✓ |
| Keep Awake · Lid Closed | Keep working with the lid closed | | ✓ |

The table follows the [pricing table on liwu.app](https://liwu.app/#pricing) row for row.

**Charging targets:** choose 20–100% on supported Macs. Targets below 80% require a successful capability check; if support is unavailable or uncertain, new targets remain at 80–100%. Lower targets may actively discharge the battery while plugged in, and the stopping level can differ from the percentage macOS displays. Liwu checks submitted targets; macOS and the battery hardware determine the actual charging behavior. For targets below 80% or Sailing, the battery bar also shows a raw capacity estimate when it differs from the macOS percentage, with an explanation button for the difference.

**Top Up (Pro):** requests 100% while keeping your regular target. Start it yourself, or let a plan start it at a set time. It ends when you turn it off or unplug, and charging returns to your regular target.

**Sailing (Pro):** keep your regular limit as the upper endpoint and choose a 5–20 percentage-point drop before recharging, with a lower endpoint of at least 20%. Firmware support must be confirmed first, even for limits of 80% or higher. The interval uses raw battery capacity, which can differ from the displayed percentage. Top Up temporarily suspends Sailing; calibration restores it when returning to the regular target.

**Calibration:** charge to full, discharge to 10%, recharge, hold for one hour, and return to your regular target. Start manually or from a schedule. Calibration requires connected power, supported low-target control, and Optimized Battery Charging turned off.

**Plans (Pro):** set a regular target, start Top Up, or start calibration at a time you choose: once, daily, weekly, biweekly, or monthly. A Top Up plan starts only if power is connected at that time; otherwise that run is skipped. Preview the next plan, skip it once, or disable it from the popover. Plans run while Liwu is running and the Mac is awake; a plan that was missed can catch up within 24 hours if you turn that on.

**Optimized Battery Charging:** keep it off while Liwu manages charging. Liwu turns it off once at first startup; if it is turned back on later in System Settings, Liwu shows a warning and lets you turn it off again.

**Keep Awake:** set an auto-off timer or a low-battery threshold. Low-battery protection applies while running on battery power and also prevents starting at or below the configured threshold. Liwu explains why a session stopped; historical stop notices can be dismissed.

**Battery health:** Liwu records maximum capacity and cycle count once a day while it is running and charts them over time. Days when Liwu was not running are left out. Readings are stored only on your Mac, together with a hash of the battery's serial number that is used to notice a replaced battery; you can export them as CSV or clear them.

**Notifications:** off until you turn them on in General or with the switch on the Schedule, Charge Control, or Keep Awake page. Liwu can tell you when calibration finishes or ends early, when a plan does not run, when Keep Awake turns itself off, and when charging control needs attention. Notifications are created on your Mac and are sent only while Liwu is running. Since 2.7.0 Liwu can also warn at a battery level you choose: once when the Mac reaches it while running on battery, and when a connected accessory that reports its battery level to macOS runs low. Those accessories are listed with their level in the menu bar popover.

**Menu bar:** sort icons into three groups inside Liwu. Click the arrows that Liwu adds to the menu bar to show or hide the Hidden group; right-click them for Menu Bar settings. Icons in Always Hidden stay out of the menu bar until you move them to another group. Restore an icon by dragging it back to Visible. Liwu and fixed system controls stay visible. Quitting reveals every group; another app or system restart may require regrouping. On a crowded menu bar with a display notch, macOS may not accept a move whose drop point falls behind the notch; Liwu reports that the move was not confirmed and leaves the groups unchanged.

Schedules and calibration require Liwu to remain running. Closing its window keeps it running; quitting ends calibration and requests release of Liwu's charging control. The helper exits once cleanup is confirmed and no new session or operation needs it. Unresolved cleanup retains its recovery state.

**Homebrew removal:** `brew uninstall --cask liwu` quits Liwu and runs its controlled cleanup before removing the app, unregistering the helper and login item. Removal stops if cleanup fails. Preferences and licenses are retained. Homebrew upgrades and reinstalls run the same cleanup; re-enable **Launch at login** afterward if you use it.

[Liwu Pro](https://liwu.app/#pricing) is a $9.99 one-time purchase with no subscription. Existing Liwu 1 Pro purchases also unlock Liwu 2 Pro.

## About this repository

This repository distributes signed installers and hosts public issue reports. Liwu's source code is private. Download the DMG attached to a release; GitHub's automatically generated source archives do not contain the app.

## Links

- [Website](https://liwu.app/?utm_source=github&utm_medium=readme)
- [Changelog](https://liwu.app/changelog?utm_source=github&utm_medium=readme)
- [Liwu 1 Legacy](https://liwu.app/legacy)
- [Report an issue](https://github.com/urfreespace/liwu-releases/issues)

---

© 2026 Liwu. All rights reserved. "Liwu" and the Liwu icon are trademarks of their owner.
