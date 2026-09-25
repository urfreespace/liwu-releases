<p align="center">
  <img src="https://liwu.app/app-icon.png" width="96" alt="Liwu icon">
</p>

<h1 align="center">Liwu</h1>
<p align="center"><b>Small tools for your MacBook, right in the menu bar.</b><br>
Charging targets, Sailing, live power, Keep Awake, calibration, schedules, and menu bar organization.</p>

<p align="center">
  <img src="https://liwu.app/screenshots/v2-popovers/battery-popover-current.png" width="330" alt="Liwu 2 Battery tab with power readings, calibration progress, and Keep Awake">
  <img src="https://liwu.app/screenshots/v2-popovers/menu-popover-current.png" width="330" alt="Liwu 2 Menu Bar tab with Hidden and Visible icon groups">
</p>

## Choose your version

| Version | Requirements | Download |
|---|---|---|
| **Liwu 2** | Apple Silicon MacBook, **macOS 26.7 or later** | [Latest release](https://github.com/urfreespace/liwu-releases/releases/latest) |
| **Liwu 1 Legacy** | Apple Silicon MacBook, macOS 14 through versions before 26.7 | [Legacy website](https://liwu.app/legacy) · [1.0.8 installer](https://github.com/urfreespace/liwu-releases/releases/download/v1.0.8/Liwu-1.0.8.dmg) |

Liwu 1 is frozen and receives no further feature updates. Do not install it on macOS 26.7 or later.

## Install Liwu 2

With Homebrew:

```sh
brew install --cask urfreespace/liwu/liwu
```

Or download the DMG from [Releases](https://github.com/urfreespace/liwu-releases/releases/latest), open it, and drag Liwu to Applications.

On first launch, follow the prompts to approve Liwu's background component. Charging control needs this component. Menu bar organization separately requests Accessibility and Screen Recording permissions when you use it to read and move icons.

Releases are signed with a Developer ID certificate and notarized by Apple. Updates are available inside the app.

## What Liwu 2 does

| Feature | Free | Pro |
|---|:---:|:---:|
| Charging targets and named presets | ✓ | ✓ |
| Adapter input and battery charging/discharging power | ✓ | ✓ |
| Keep Awake with the lid open | ✓ | ✓ |
| Drag menu bar icons between Hidden and Visible groups | ✓ | ✓ |
| Top Up to temporarily request 100% | | ✓ |
| Sailing charging range | | ✓ |
| Five-step battery calibration | | ✓ |
| Scheduled charging targets and calibration | | ✓ |
| Keep Awake with the lid closed | | ✓ |

**Charging targets:** choose 20–100% on supported Macs. Targets below 80% require a successful capability check; if support is unavailable or uncertain, new targets remain at 80–100%. Lower targets may actively discharge the battery while plugged in, and the stopping level can differ from the percentage macOS displays. Liwu checks submitted targets; macOS and the battery hardware determine the actual charging behavior.

**Sailing (Pro):** keep your regular limit as the upper endpoint and choose a 5–20 percentage-point drop before recharging, with a lower endpoint of at least 20%. Firmware support must be confirmed first, even for limits of 80% or higher. The interval uses raw battery capacity, which can differ from the displayed percentage. Top Up temporarily suspends Sailing; calibration restores it when returning to the regular target.

**Calibration:** charge to full, discharge to 10%, recharge, hold for one hour, and return to your regular target. Start manually or from a schedule. Calibration requires connected power, supported low-target control, and Optimized Battery Charging turned off.

**Keep Awake:** set an auto-off timer or a low-battery threshold. Low-battery protection applies while running on battery power and also prevents starting below the configured threshold. Liwu explains why a session stopped; historical stop notices can be dismissed.

**Menu bar:** manage icons inside Liwu, use the eye button to temporarily reveal the hidden group, and restore icons by dragging them back to Visible. Liwu and fixed system controls stay visible. Quitting reveals the hidden group; another app or system restart may require regrouping.

Schedules and calibration require Liwu to remain running. Closing its window keeps it running; quitting ends calibration and requests release of Liwu's charging control.

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
