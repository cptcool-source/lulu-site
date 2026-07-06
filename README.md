# Lens &amp; Lu — Photography Site

**Brand:** Lens &amp; Lu · family &amp; couples photographer, Coastal California
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
├── assets/           # lulu-logo.png, lulu-portrait.png, lulu-painting.jpg
├── CLAUDE.md         # project stack + brand lock
└── README.md
```

## Style lock — "Sunbaked Clay, dark-first" (locked 2026-07-06)

Archetype: **Free Spirit · Lover · Creator** — *"the last 40 minutes of daylight."*
Motion vocabulary (closed set): **drift · bloom · grain.**

- **3-hex lock:** ground umber `#2E2118` · text cream `#F4EDE1` · accent terracotta `#C8613C`
  (action / large display only — never body). Light sections = the same three hexes inverted.
- **Supporting neutrals** (outside the lock): sage `#8A9A7B`, sand `#E0D3BE`.
- **Type:** Instrument Serif (display, italic) + Hanken Grotesk (body).
- Its **own identity** — not the chuck design brand (no Outfit/coral, no Pixel mark; Fraunces banned).

*(The current `index.html` still ships the pre-lock plum/Cormorant export — rebuild to this lock is pending; real photography required before styling.)*

## Local preview

Serve over HTTP so `support.js` / `image-slot.js` load correctly:

```bash
python -m http.server 8000   # then open http://localhost:8000
# or: npx serve .
```

## Deploy

GitHub Pages (Path A default). Repo + remote + Pages **not set up yet** — pending go-ahead.
