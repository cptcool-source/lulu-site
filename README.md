# LuLu &amp; Lens — Photography Site

**Brand:** LuLu &amp; Lens · family &amp; couples photographer, Coastal California
**Owner:** Charles Spivey / chuck design (build)
**Live site:** _not deployed yet — GitHub Pages target_

---

## Project

A single-page portfolio / booking site for LuLu &amp; Lens, a family and couples
photographer ("Every family has a story worth keeping — MEMORIES captured FOREVER").
Sessions: Beach · Home · Golden Hour. Primary action: **inquire / book a session**
(`hello@luluandlens.com`).

Originated as a **claude.ai Design Composer export** (`.dc.html`), renamed to `index.html`
as the web entry point. The original export is preserved in `../lulu-site.zip`.

---

## Tech Stack — Path A (Vanilla, no build step)

| Layer | Choice |
|---|---|
| Markup | Single-file `index.html`, inline styles (design-composer output) |
| Runtime | `support.js` — claude Design Composer support runtime (required) |
| Components | `image-slot.js` — `<x-import>` drop-photo web component for the portfolio grid |
| Fonts | Cormorant Garamond (display, italic) + Mulish (body) — Google Fonts |
| Images | `assets/` — logo, portrait, painting; portfolio slots are drop-in via image-slot |
| Hosting | Static — GitHub Pages ready (serve over HTTP, not `file://`) |

## Structure

```
lulu-site/
├── index.html        # entry point (was "LuLu & Lens.dc.html")
├── support.js        # design-composer runtime — do not remove
├── image-slot.js     # drop-photo web component (portfolio grid)
├── assets/           # lulu-logo.png, lulu-portrait.png, lulu-painting.jpg
├── CLAUDE.md         # project stack + brand lock
└── README.md
```

## Brand tokens (observed from the export — confirm before locking)

- **Palette:** plum/ink `#221b2c` · `#2f2836` · `#6f5c92` · lavender `#b9abc9` /
  `#d5c7ea` / `#c9b8e2` · cream `#f4efe9` · champagne-gold `#e6d6a8` / `#9a7d3f`
- **Type:** Cormorant Garamond (italic display) + Mulish (body)
- Its **own identity** — not the chuck design brand (no Outfit/coral, no Pixel mark).

## Local preview

Serve over HTTP so `support.js` / `image-slot.js` load correctly:

```bash
python -m http.server 8000   # then open http://localhost:8000
# or: npx serve .
```

## Deploy

GitHub Pages (Path A default). Repo + remote + Pages **not set up yet** — pending go-ahead.
