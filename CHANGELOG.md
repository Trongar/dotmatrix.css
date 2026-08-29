# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.0] - 2026-08-29

### Added
- **8 texture patterns** (`data-texture="..."`) opt-in via attribute, no classes:
  - `paper` — recycled paper grain
  - `dots` — graph paper / engineering pad
  - `stripes` — diagonal 45° stripes
  - `hatch` — cross-hatch / woven fabric
  - `halftone` — newsprint photo dots
  - `noise` — xerox / photocopy grain
  - `carbon` — gradient + grain combo
  - `phosphor` — CRT RGB dot pattern
- **5 texture presets** (`data-texture-preset="..."`):
  - `sepia`, `vintage`, `phosphor`, `subtle`, `strong`
- **2 bevel effects** (`data-bevel="in"` / `data-bevel="out"`) for 3D pressed/raised look
- **New CSS variables**: `--dm-texture`, `--dm-texture-color`, `--dm-surface-2`, `--dm-border-light`, `--dm-border-dark`
- **Emoji monochrome rendering** via `font-variant-emoji: text` (default), override with `--dm-emoji-style`
- **10 demo apps** in `demos/` showcasing the framework across wildly different themes
- **Showcase hub** in `showcase/` linking all demos with texture/bevel previews
- **Desktop-first responsive** in all demos (1100/900/700/600px breakpoints, max-width collapsing only)

### Changed
- Default body now applies `font-variant-emoji: text` so emojis render as monochrome wireframes
- Beveled surfaces use a 3-layer shadow system (inset highlight + inset shadow + outer drop) instead of flat borders

### Notes
- `dotmatrix.css` size: 5.2 KB gzipped (was ~5 KB) — textures cost ~200 bytes total
- All demos are desktop-first responsive: collapse to mobile gracefully without losing aesthetic density
- HTML remains 100% semantic — `data-texture` and `data-bevel` are opt-in attributes, never classes

## [0.1.0] - 2026-08-28

### Added
- Initial release
- Light theme (default)
- Dark theme via `data-theme="dark"`
- Support for all semantic HTML elements
- Custom CSS variables for theming
- Scanline overlay effect
- Responsive design
- Demo page showcasing all components
