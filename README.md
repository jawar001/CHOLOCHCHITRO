# Cholochchitro — A Timeline of Bangladesh Cinema

> **চলচ্চিত্রের যাত্রা** — From *Mukh O Mukhosh* (1956) to the streaming age.
> An interactive, single-file animated timeline of seventy years of Bangladeshi cinema.

**Live site:** <https://jawar001.github.io/CHOLOCHCHITRO/>

---

## What it is

A cinematic, scroll-driven story of Bangladesh's cinema from its very first feature film
in 1956 to the festival-and-streaming era of today. Visitors can:

- **Drag a time-machine scrubber** from 1956 → 2026 to travel between eras
- **Click any year tick** (1956 / 1970 / 1985 / 2000 / 2010 / 2026) to jump
- **Use the keyboard** (← → Home End) on the scrubber for accessibility
- **Scroll** normally — the scrubber syncs back to your scroll position

The page is broken into six chapters of national cinema history, then galleries of
ten **Legendary Actors** and ten **Visionary Directors**.

## The six eras

| # | Years | Title | Anchor |
|---|---|---|---|
| I   | 1956–1969 | The First Light             | *Mukh O Mukhosh* — the country's first feature film |
| II  | 1970–1979 | Liberation & the New Wave   | *Jibon Theke Neya*, *Stop Genocide*, *Ora Egaro Jon* |
| III | 1980–1995 | The Golden Age              | *Beder Meye Josna*, the Razzak / Salman Shah era |
| IV  | 1996–2005 | Transition                  | Parallel cinema rises; *Matir Moina* at Cannes |
| V   | 2006–2015 | The Renaissance             | Farooki, multiplexes, festival circuit |
| VI  | 2016–today | The New Frontier           | *Aynabaji*, *Doob*, *Hawa*, *Saturday Afternoon* |

## Tech

- **One file**, `index.html` — all CSS, JS, and SVG art inlined
- **No build step**, **no external JavaScript** dependencies
- Google Fonts: *Playfair Display* (display), *Inter* (body), *Bebas Neue* (marquee), *Hind Siliguri* (Bangla)
- **Animations** via CSS keyframes + `IntersectionObserver` — film grain, projector flicker,
  staggered entrance reveals, sticky two-way-bound timeline scrubber
- **Accessible**: keyboard-driven scrubber with ARIA `role="slider"`, semantic landmarks,
  visible focus rings, and `prefers-reduced-motion` respected throughout
- **Responsive**, mobile-first, breakpoints at 640 / 1024 px

Design tokens live in [`design-system.json`](./design-system.json) and as CSS custom
properties in `:root` inside `index.html`.

## Run it locally

The site is a static HTML file in `docs/`, so any of these works:

```bash
# Option 1 — open directly
xdg-open docs/index.html   # Linux
open docs/index.html       # macOS
start docs/index.html      # Windows

# Option 2 — serve over HTTP (recommended; some browsers restrict file://)
python3 -m http.server 8765 --directory docs
# then visit http://localhost:8765/
```

## GitHub Pages

This repository is published with **GitHub Pages** from `main` / `docs`:

```
https://jawar001.github.io/CHOLOCHCHITRO/
```

To change the source: *Repo → Settings → Pages → Branch: `main` / `/docs`*.

## Credits

Curated, written, and designed by **Shahajada Jawar** (`@jawar001`).
A love letter to Bangladeshi cinema, 1956–2026.

Historical notes draw on widely-published sources about the careers of
Abdul Jabbar Khan, Zahir Raihan, Razzak, Kabori, Shabana, Salman Shah, Tareque Masud,
Mostofa Sarwar Farooki and others; any errors are the curator's own — pull requests welcome.

## License

Code released under the MIT License — feel free to fork, remix, and re-tell the story.
