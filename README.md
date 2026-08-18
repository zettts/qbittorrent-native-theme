# qBittorrent Native Theme

A clean, compact qBittorrent theme pack with monochrome icons and platform-oriented light/dark variants for macOS, Windows, and Linux.

> Current release: **v1.0**  
> Built around qBittorrent 5.x.

![qBittorrent Native preview](assets/preview.png)

## Themes

| Platform | Light | Dark | Status |
|---|---|---|---|
| macOS | `themes/macos-light.qbtheme` | `themes/macos-dark.qbtheme` | Light tested on 5.2.3; Dark beta |
| Windows | `themes/windows-light.qbtheme` | `themes/windows-dark.qbtheme` | Beta |
| Linux | `themes/linux-light.qbtheme` | `themes/linux-dark.qbtheme` | Beta / needs wider distro testing |

## Features

- Compact 24 px monochrome toolbar icons
- Matching Preferences/sidebar icon set
- Light and dark variants
- Platform-specific QSS rather than one universal stylesheet
- Reduced visual clutter and restrained accent colors
- No SF Symbols or proprietary Apple icon assets; the SVG set is custom-made

## Installation

1. Download the `.qbtheme` file for your platform and color mode from `themes/`.
2. Open qBittorrent.
3. Go to **Tools / Preferences -> Behavior -> Interface**.
4. Enable **Use custom UI Theme** and select the `.qbtheme` file.
5. Fully quit qBittorrent and launch it again.

For the best Dark result, set the operating system itself to Dark mode before launching qBittorrent.

## Source layout

Each folder under `source/` contains:

- `stylesheet.qss`
- `config.json`
- `resources.qrc`
- `icons/` SVG resources

The compiled `.qbtheme` files are kept separately in `themes/` for simple installation.

## Compatibility notes

qBittorrent is a Qt application, so some widget metrics and native controls can differ between Qt versions and operating systems. Dark mode is especially sensitive to the system palette. The theme intentionally avoids overly broad `QWidget` recoloring where it conflicts with native platform controls.

The macOS build contains additional toolbar-spacing adjustments because qBittorrent inserts spacer widgets in the unified macOS toolbar.

## Known limitations

- Light/Dark switching is not automatic; select the corresponding `.qbtheme` manually.
- Linux appearance can vary between desktop environments and Qt styles.
- macOS titlebar appearance is controlled by macOS and requires the matching system appearance.
- Some qBittorrent versions may use slightly different resource names or widget metrics.

## License

Theme code and custom SVG icons in this repository are released under the MIT License. qBittorrent is a separate project and is not affiliated with this theme.
