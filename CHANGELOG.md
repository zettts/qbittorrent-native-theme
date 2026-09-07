# Changelog

## 2.0 - 2026-09-07

- Replaced the six per-platform builds (macOS/Windows/Linux × Light/Dark) with two OS-agnostic builds: `light.qbtheme` and `dark.qbtheme`.
- Source audit found `config.json` was empty (`{}`) in all six previous builds, icon SVGs were geometrically identical across platforms (only a hardcoded stroke color differed), and the one real cross-platform fix (toolbar separator/QToolButton workaround) was already copy-pasted verbatim into every variant.
- Dark theme now forces its own app-wide palette (QWidget/QTreeView/QLineEdit/QMenu/QTabWidget/QScrollBar) instead of relying on the OS being set to dark mode first.
- Unified accent color and corner-radius across both themes.
- `source/` now has two folders (`light/`, `dark/`) instead of six.

## 1.0 - 2026-08-12

- First GitHub-ready release package.
- Added macOS Light and Dark variants.
- Added Windows Light and Dark variants.
- Added Linux Light and Dark variants.
- Added compact monochrome toolbar icon set.
- Added matching Preferences/sidebar icons.
- Added source QSS, QRC, JSON and SVG files for all variants.
