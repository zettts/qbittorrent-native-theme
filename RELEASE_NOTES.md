# qBittorrent Native Theme v2.0

Consolidated release: two OS-agnostic builds instead of six per-platform ones.

Included builds:

- Light (`themes/light.qbtheme`)
- Dark (`themes/dark.qbtheme`)

Why the change: a source-level audit of the previous six builds found `config.json` unused (empty in every variant), the icon SVGs identical in geometry across platforms (only the color differed), and the toolbar-separator/QToolButton fix already duplicated byte-for-byte into every stylesheet rather than being platform-specific. The real remaining differences were a couple of color values and a border-radius — not enough to justify six separate builds. Dark mode was rebuilt to force its own palette so it no longer depends on the OS being set to dark first.

The previous macOS Light build was the only one independently verified against a running qBittorrent instance; that verification carries forward into both v2.0 builds for the toolbar-specific fix. Wider testing across distros/Qt styles is still welcome via issues.
