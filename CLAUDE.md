# Lens &amp; Lu

## Stack — Path A (Vanilla, no build step)
- Single-file `index.html` with inline styles — originated as a claude Design Composer
  export (`.dc.html`). No framework, no bundler, static host (GitHub Pages).
- `support.js` — Design Composer support runtime. **Required by index.html — do not remove.**
- `image-slot.js` — defines the `image-slot` web component used via
  `<x-import component-from-global-scope="image-slot" from="./image-slot.js">` for the
  portfolio grid's drop-photo slots.
- Fonts: **Instrument Serif** (display, incl. italic) + **Hanken Grotesk** (body) via Google
  Fonts. (Pre-lock export used Cormorant Garamond + Mulish — being replaced in the rebuild.)
- Serve over HTTP for local preview (`python -m http.server`) — `file://` breaks the imports.

## Archetype & Feel (locked 2026-07-06)
- Archetype: **Free Spirit (Explorer) · Lover · Creator.** Feel: *"the last 40 minutes of
  daylight"* — warm, slow, film, a little overexposed; nothing in a hurry. The one fast beat
  is user-caused (hover / click).
- Motion vocabulary is a CLOSED set — only these three ship: **drift · bloom · grain.**
- Signature moment: scrolling into the portfolio, the ground scrubs cream → umber, a warm
  light-leak blooms, grain resolves, and the photographs ignite on the dark.

## Style Lock — "Sunbaked Clay, dark-first" (locked 2026-07-06 · exactly 3 hexes)
- Lens & Lu's OWN identity — NOT chuck design house style (no Outfit, no coral `#E05C3A`, no
  Pixel mark). **Fraunces banned. Cormorant retired.**
- **Ground** `#2E2118` umber (dark-first) · **Text** `#F4EDE1` cream · **Accent** `#C8613C`
  terracotta. The light rendering (cream ground / umber text) is the SAME three hexes
  inverted — used for breathing-room / contrast sections only.
- **Accent rule:** terracotta is for ACTION and large display ONLY (~3:1 on umber) — never
  body copy. Body is always cream-on-umber (or umber-on-cream) — both safe.
- Supporting neutrals (NOT part of the 3-lock; use sparingly): sage `#8A9A7B`, sand `#E0D3BE`.
- Type: **Instrument Serif** (display, incl. italic) + **Hanken Grotesk** (body).

## Project Context
Single-page portfolio + booking site for Lens &amp; Lu, a family &amp; couples photographer
in Coastal California. Voice is warm and personal ("I photograph the in-between moments").
Sessions: Beach · Home · Golden Hour. Primary CTA: **inquire / book a session**
(`hello@lensandlu.com`); Instagram is the secondary channel.

## Working Rules
- Honesty brand still applies: no fake reviews, no fake scarcity; any placeholder contact
  info must be inert / non-routable until real details are confirmed.
- Immutable-cached assets change under a NEW filename on every content change.
- Commit when Charles says commit; deploy when Charles says deploy. GitHub repo/remote and
  Pages are not set up yet.
