# LuLu &amp; Lens

## Stack — Path A (Vanilla, no build step)
- Single-file `index.html` with inline styles — originated as a claude Design Composer
  export (`.dc.html`). No framework, no bundler, static host (GitHub Pages).
- `support.js` — Design Composer support runtime. **Required by index.html — do not remove.**
- `image-slot.js` — defines the `image-slot` web component used via
  `<x-import component-from-global-scope="image-slot" from="./image-slot.js">` for the
  portfolio grid's drop-photo slots.
- Fonts: **Cormorant Garamond** (italic display) + **Mulish** (body) via Google Fonts.
- Serve over HTTP for local preview (`python -m http.server`) — `file://` breaks the imports.

## Brand Constraints (LuLu &amp; Lens — its OWN identity, not chuck design)
- This is a client/concept brand and carries its own locks. **Do NOT** apply chuck design
  house style (no Outfit, no coral `#E05C3A`, no Pixel mark, Fraunces still banned).
- Palette (observed from export — confirm before treating as a hard lock):
  ink/plum `#221b2c` · `#2f2836` · `#6f5c92` · lavender `#b9abc9` / `#d5c7ea` / `#c9b8e2` ·
  cream `#f4efe9` · champagne-gold `#e6d6a8` / `#9a7d3f`.
- Type: Cormorant Garamond + Mulish.

## Project Context
Single-page portfolio + booking site for LuLu &amp; Lens, a family &amp; couples photographer
in Coastal California. Voice is warm and personal ("I photograph the in-between moments").
Sessions: Beach · Home · Golden Hour. Primary CTA: **inquire / book a session**
(`hello@luluandlens.com`); Instagram is the secondary channel.

## Working Rules
- Honesty brand still applies: no fake reviews, no fake scarcity; any placeholder contact
  info must be inert / non-routable until real details are confirmed.
- Immutable-cached assets change under a NEW filename on every content change.
- Commit when Charles says commit; deploy when Charles says deploy. GitHub repo/remote and
  Pages are not set up yet.
