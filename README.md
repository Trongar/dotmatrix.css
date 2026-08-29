# crt-design-system

**Classless pixel-art CSS framework** — write semantic HTML, get a retro CRT interface for free.

![Version](https://img.shields.io/badge/version-0.2.0-006600?style=flat-square)
![Size](https://img.shields.io/badge/size-~5KB%20gzipped-006600?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-006600?style=flat-square)

## Features

- **Classless** — zero classes required, styles semantic HTML directly
- **Lightweight** — ~5KB gzipped, no JavaScript
- **Retro aesthetic** — pixel-art UI with CRT terminal vibes
- **Themeable** — CSS variables for full customization
- **Textured** — 8 paper/grain/dot patterns via `data-texture` attribute
- **Beveled** — 3D pressed/raised surfaces via `data-bevel` attribute
- **Accessible** — proper focus states, semantic structure, captions on tables, labeled navs
- **Responsive** — desktop-first, collapses gracefully on smaller screens

## Quick Start

### CDN

```html
<link rel="stylesheet" href="https://unpkg.com/crt.css@0.2.0/crt.css">
```

### npm

```bash
npm install crt.css
```

```javascript
import 'crt.css/crt.css';
```

### Manual

Download [`crt.css`](./crt.css) and link it:

```html
<link rel="stylesheet" href="crt.css">
```

## Usage

Just write semantic HTML:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <link rel="stylesheet" href="crt.css">
</head>
<body>
  <header>
    <h1>My Retro App</h1>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
      </ul>
    </nav>
  </header>
  
  <main>
    <article>
      <h2>Welcome</h2>
      <p>This is a paragraph with <strong>bold</strong> and <em>italic</em>.</p>
      <button>Click me</button>
    </article>
  </main>
</body>
</html>
```

That's it. No classes, no JavaScript, no build step.

## Textures

Apply any of 8 texture patterns to any element with a single attribute:

```html
<article data-texture="paper">...</article>     <!-- recycled paper grain -->
<section data-texture="dots">...</section>      <!-- graph paper -->
<div data-texture="halftone">...</div>          <!-- newsprint photo -->
<aside data-texture="hatch">...</aside>         <!-- cross-hatch weave -->
<header data-texture="stripes">...</header>     <!-- 45° stripes -->
<footer data-texture="noise">...</footer>       <!-- xerox grain -->
<div data-texture="carbon">...</div>            <!-- gradient + grain -->
<main data-texture="phosphor">...</main>       <!-- CRT RGB dots -->
```

### Presets

Quick combos for common aesthetics:

```html
<body data-texture-preset="vintage">  <!-- strong brown grain -->
<body data-texture-preset="sepia">    <!-- subtle warm grain -->
<body data-texture-preset="phosphor"> <!-- for dark themes -->
<body data-texture-preset="subtle">   <!-- barely there -->
<body data-texture-preset="strong">   <!-- pronounced -->
```

## Bevels

3D pressed or raised look with a single attribute:

```html
<button data-bevel="out">Raised button</button>
<input data-bevel="in" type="text">          <!-- sunken input -->
<div data-bevel="out">Raised panel</div>
```

## Themes

### Light (default)

```html
<body>
  <!-- Light theme is automatic -->
</body>
```

### Dark

```html
<body data-theme="dark">
  <!-- Dark theme activated -->
</body>
```

## Customization

Override CSS variables to create your own theme:

```css
:root {
  --crt-bg: #1a1a2e;
  --crt-accent: #ff6b6b;
  --crt-text: #eaeaea;
  --crt-font-size: 14px;
  --crt-texture: 1;
  --crt-texture-color: rgba(255, 100, 100, 0.15);
}
```

All available variables:

```css
:root {
  /* Colors */
  --crt-bg: #f0f0e8;
  --crt-surface: #e8e8e0;
  --crt-surface-2: #dcdcd0;          /* NEW: deeper surface variant */
  --crt-border: #b0b0a0;
  --crt-border-light: #d0d0c0;      /* NEW: bevel highlight */
  --crt-border-dark: #808070;       /* NEW: bevel shadow */
  --crt-text: #1a1a1a;
  --crt-text-muted: #666655;
  --crt-accent: #006600;
  --crt-accent-dim: #004400;
  --crt-accent-alt: #aa6600;
  --crt-danger: #cc0000;
  --crt-success: #006600;

  /* Typography */
  --crt-font: 'Courier New', monospace;
  --crt-font-size: 13px;
  --crt-line-height: 1.6;
  --crt-heading-font: 'Courier New', monospace;

  /* Spacing */
  --crt-space-xs: 4px;
  --crt-space-sm: 8px;
  --crt-space-md: 16px;
  --crt-space-lg: 24px;
  --crt-space-xl: 32px;
  --crt-space-2xl: 48px;

  /* Borders */
  --crt-border-width: 2px;
  --crt-radius: 0px;
  --crt-pixel: 2px;                  /* stepped shadow offset */

  /* Effects */
  --crt-scanlines: 1;                /* 0-2, scanline intensity */
  --crt-texture: 0;                  /* 0-2, texture intensity */
  --crt-texture-color: rgba(0,0,0,0.08);
  --crt-emoji-style: text;           /* text | emoji | unicode */
  --crt-max-width: 800px;
}
```

## Demos

See crt.css in action across 10 real-world apps:

1. **[Landing page](demos/01-landing.html)** — marketing site
2. **[Auth flows](demos/02-auth.html)** — sign-in / sign-up / 2FA
3. **[SaaS dashboard](demos/03-dashboard.html)** — CRM with sidebar + KPI + charts
4. **[Pricing](demos/04-pricing.html)** — tiered plans + comparison
5. **[Long-form essay](demos/05-blog.html)** — blog/article with TOC
6. **[Library catalog](demos/06-library.html)** — book grid with filters
7. **[Bakery](demos/07-cakes.html)** — pastry shop with order form
8. **[IRC / BBS social](demos/08-social.html)** — chat + forum threads
9. **[Encyclopedia](demos/09-encyclopedia.html)** — Encarta-style article
10. **[Running tracker](demos/10-running.html)** — GPS map + stats + training calendar

**Showcase hub**: [showcase/index.html](showcase/index.html) — links all 10 with texture/bevel previews.

Each demo uses a different theme via CSS variable overrides. Same HTML semantics, radically different vibes.

## Browser Support

- Chrome/Edge (last 2 versions)
- Firefox (last 2 versions)
- Safari (last 2 versions)

`data-texture` and `data-bevel` use only standard CSS (gradients, box-shadow) — works everywhere.

`font-variant-emoji: text` requires Chrome 131+, Firefox 132+, Safari 18.2+. Falls back gracefully to native emoji on older browsers.

## Inspiration

- [Spidey Tracker](https://spideytracker.com/) — Sony/Samsung promotional site with CRT terminal aesthetic
- [NES.css](https://nostalgic-css.github.io/NES.css/) — 8-bit CSS framework (requires classes)
- [Pico CSS](https://picocss.com/) — classless CSS framework
- [Water.css](https://watercss.kognise.dev/) — minimal classless stylesheet

## Philosophy

**Less is more.** You shouldn't need to add `class="btn btn-primary"` to every button. Your HTML tags already have semantic meaning — let them style themselves.

crt.css exists because:
1. Existing pixel-art frameworks (NES.css) require verbose class names
2. Classless frameworks (Pico, Water) lack retro aesthetics
3. Building retro UIs from scratch wastes tokens and time
4. **No other framework combines classless + pixel-art + textures + bevels in one small file**

## Development

```bash
# View the main demo
open demo.html

# View the showcase hub
open showcase/index.html

# View individual demos
open demos/03-dashboard.html
```

No build step. It's just CSS.

## Contributing

Issues and PRs welcome. Keep it simple, keep it classless.

## License

MIT © 2026
