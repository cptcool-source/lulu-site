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

## Style Lock — moody palette (client pivot 2026-07-06 · supersedes "Sunbaked Clay")
- Client (Dana) rejected orange — a hard pivot away from terracotta. Lens & Lu's OWN
  identity, NOT chuck design house style. **Fraunces banned. Cormorant retired. No orange.**
- **Grounds (dark):** olive `#3A3A2A` (main — hero, sessions, gallery) · plum `#322A3A`
  (contact) · deep plum `#26202E` (footer) · slate `#2A323A` (modal). These near-equal-value
  darks set the mood; they cannot carry text or a high-contrast accent on their own.
- **Text:** cream `#F4EDE1`. **Light "breathing" sections** (About, Process) invert to a
  cream ground with olive `#3A3A2A` text.
- **Accent:** lavender `#C3B4D6` — eyebrows, italic accent words, stats, hover, the "— Dana"
  pill. Same lavender on the cream sections (low-contrast by design; Charles eye-checked).
- **Buttons:** cream-filled + olive text (no colored accent button). Scroll-nav = **cream**
  bar with olive text/logo + an olive (dark) book button.
- Motion (drift · bloom · grain) glow cooled to a soft **lavender-white**, not gold.
- Type: **Instrument Serif** (display, incl. italic) + **Hanken Grotesk** (body). Two fonts.
- This is a **5-tone system** (3 dark grounds + cream + lavender), sanctioned by the client's
  palette choice — no longer the exactly-3-hex lock.

## Project Context
Single-page portfolio + booking site for Lens &amp; Lu, a family &amp; couples photographer
in Southwest Florida. Voice is warm and personal ("I photograph the in-between moments").
Sessions: Beach · Home · Golden Hour. Primary CTA: **inquire / book a session**
(`hello@lensandlu.com`); Instagram is the secondary channel.

## Working Rules
- Honesty brand still applies: no fake reviews, no fake scarcity; any placeholder contact
  info must be inert / non-routable until real details are confirmed.
- Immutable-cached assets change under a NEW filename on every content change.
- Commit when Charles says commit; deploy when Charles says deploy. GitHub repo/remote and
  Pages are not set up yet.
