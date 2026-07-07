# Lens &amp; Lu — Photography Site

**Brand:** Lens &amp; Lu · family &amp; couples photographer, Southwest Florida
**Owner:** Charles Spivey / chuck design (build)
**Live site:** _not deployed yet — GitHub Pages target_

---

## Project

A single-page portfolio / booking site for Lens &amp; Lu, a family and couples
photographer ("Every family has a story worth keeping — MEMORIES captured FOREVER").
Sessions: Beach · Home · Golden Hour. Primary action: **inquire / book a session**
(`hello@lensandlu.com`).

Originated as a **claude.ai Design Composer export** (`.dc.html`), renamed to `index.html`
as the web entry point. The original export is preserved in `../lulu-site.zip`.

---

## Tech Stack — Path A (Vanilla, no build step)

| Layer | Choice |
|---|---|
| Markup | Single-file `index.html`, inline styles (design-composer output) |
| Runtime | `support.js` — claude Design Composer support runtime (required) |
| Components | `image-slot.js` — `<x-import>` drop-photo web component for the portfolio grid |
| Fonts | Instrument Serif (display, italic) + Hanken Grotesk (body) — Google Fonts |
| Images | `assets/` — logo, portrait, painting; portfolio slots are drop-in via image-slot |
| Hosting | Static — GitHub Pages ready (serve over HTTP, not `file://`) |

## Structure

```
lulu-site/
├── index.html        # entry point (was "LuLu & Lens.dc.html")
├── support.js        # design-composer runtime — do not remove
├── image-slot.js     # drop-photo web component (portfolio grid)
├── assets/           # dana-portrait.webp (page) + .jpg (social), lulu-logo.png
├── CLAUDE.md         # project stack + brand lock
└── README.md
```

## Style lock — moody palette (client pivot 2026-07-06, no orange)

Archetype: **Free Spirit · Lover · Creator.** Motion (closed set): **drift · bloom · grain.**

- **Grounds (dark):** olive `#3A3A2A` (main) · plum `#322A3A` (contact) · slate `#2A323A` (scroll-nav, modal).
- **Text:** cream `#F4EDE1`. Light "breathing" sections (About, Process) = cream ground + olive text.
- **Accent:** lavender `#C3B4D6` (eyebrows, italic words, stats, hover). Buttons cream-filled + olive text.
- **Type:** Instrument Serif (display, italic) + Hanken Grotesk (body).
- Its **own identity** — not chuck design (no Outfit/coral/Pixel mark; Fraunces banned; no orange).

*(Superseded the earlier terracotta "Sunbaked Clay" lock after the client rejected orange.)*

## Local preview

Serve over HTTP so `support.js` / `image-slot.js` load correctly:

```bash
python -m http.server 8000   # then open http://localhost:8000
# or: npx serve .
```

## Deploy

GitHub Pages (Path A default). Repo + remote + Pages **not set up yet** — pending go-ahead.
