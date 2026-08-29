# crt.css

**Classless pixel-art CSS framework** — write semantic HTML, get a retro CRT interface for free.

![Version](https://img.shields.io/badge/version-0.1.0-006600?style=flat-square)
![Size](https://img.shields.io/badge/size-~6KB%20gzipped-006600?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-006600?style=flat-square)

## Features

- **Classless** — zero classes required, styles semantic HTML directly
- **Lightweight** — ~6KB gzipped, no JavaScript
- **Retro aesthetic** — pixel-art UI with CRT terminal vibes
- **Themeable** — CSS variables for full customization
- **Accessible** — proper focus states, semantic structure
- **Responsive** — works on all screen sizes

## Quick Start

### CDN

```html
<link rel="stylesheet" href="https://unpkg.com/crt.css@0.1.0/crt.css">
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
<html>
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
}
```

All available variables:

```css
:root {
  /* Colors */
  --crt-bg: #f0f0e8;
  --crt-surface: #e8e8e0;
  --crt-border: #b0b0a0;
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

  /* Spacing */
  --crt-space-xs: 4px;
  --crt-space-sm: 8px;
  --crt-space-md: 16px;
  --crt-space-lg: 24px;
  --crt-space-xl: 32px;

  /* Borders */
  --crt-border-width: 2px;
  --crt-radius: 0px;

  /* Effects */
  --crt-scanlines: 1; /* 0-2, intensity of scanline overlay */
  --crt-max-width: 800px;
}
```

## Browser Support

- Chrome/Edge (last 2 versions)
- Firefox (last 2 versions)
- Safari (last 2 versions)

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

## Development

```bash
# View demo
open demo.html

# No build step needed — it's just CSS
```

## Contributing

Issues and PRs welcome. Keep it simple, keep it classless.

## License

MIT © 2026
