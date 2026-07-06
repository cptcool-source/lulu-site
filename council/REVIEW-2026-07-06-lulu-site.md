# Council Review — LuLu & Lens site — 2026-07-06

**Subject:** LuLu & Lens photography site (Path A static showcase) · `index.html`
**Question:** Is this Awwwards-worthy, and what's the ranked path to award level?
**Bench:** Portfolio, Brand, Copy, CRO, Performance, Social, SEO, Market + Chair. (`council-account` benched — no proposal/pricing/scope artifact.)
**Scores:** Copy 78 · Brand 70 · Portfolio 59 · Performance 58 · CRO 52 · Market 43 · SEO 22 · Social 18

---

## Executive summary

The council scored LuLu & Lens 18–78 (Copy strongest at 78, Social weakest at 18) — a premium-feeling craft shell wrapped around missing substance, nowhere near award level and not yet shippable. The through-line every seat circles: **a photographer's site with no photographs and no head plumbing** — the gradient hero, empty gallery cells, dead `<head>`, and faked form all say "unfinished," not "unhurried." The one decision Charles owns: source and load real photography now, or the entire top of this list is blocked behind it.

---

## Ranked punch list

### BLOCKERS — cannot ship as-is
1. **Wire the inquiry form to a real endpoint** (Formspree/Netlify) — `setTimeout` fakes "Request received"; 100% of inquiries vanish silently. `[CRO]` **M**
2. **Add a real `<head>`** — `<title>`, `<html lang="en">`, meta description, canonical, og:image (real photo), twitter card. Currently 2 meta tags; link previews dead on arrival. `[SEO+SOCIAL]` **S**
3. **Add a real `<h1>`** — visual headline is 3 styled divs (`lz-h1-*`); five `<h2>` sit under no `<h1>`. `[SEO]` **S**
4. **Recompress images to display-sized WebP under NEW filenames** — `lulu-portrait.png` (2.33MB) + `lulu-logo.png` (807KB, 25× oversized); green unachievable otherwise (3.14MB → ~150KB). `[PERF]` **M**
5. **Load real photography** into hero + the 6 empty gallery cells — empty portfolio kills desire before the CTA and caps every award axis. `[PORTFOLIO+SOCIAL+CRO+SEO]` **M**

### TO REACH AWARD LEVEL
6. **Rewrite the hero headline** — "MEMORIES/captured/FOREVER" is the #1 photographer cliché and the biggest, laziest line on the page; pull from the bio voice ("barefoot chases," "belly laughs"). `[COPY+BRAND+MARKET+PORTFOLIO]` **S**
7. **Make dead `<span>`s real** — nav needs anchors/scroll; IG + Pinterest + "Inquire for pricing" are non-clickable. `[PORTFOLIO+SOCIAL+CRO]` **M**
8. **Add mobile overrides** — services/portfolio/process are desktop `repeat(N,1fr)` with none; Process crushes unreadable. `[PORTFOLIO]` **M**
9. **Give champagne-gold ONE job** (act/booking only) — it's on CTAs, eyebrows, stats, dots, focus rings; the CTA stops pulling. `[BRAND+CRO]` **S**
10. **Cut CTA vocabulary from 5 variants to two** — "Let's do a shoot!" clashes with the unhurried brand. `[COPY+CRO+MARKET]` **S**
11. **Replace the category-generic promise** ("soulful, unhurried, honest") with ONE claim only LuLu can make; pin the headline to it. `[MARKET]` **M**
12. **Name a real market** — "Coastal California" (~840mi) signals nothing; e.g. "Santa Barbara & the Central Coast." `[MARKET]` **S**
13. **Redesign the mark** — fuzzy circular monogram-badge, illegible at 52px, dies at 16px/reversed (#1 template tell); add clear-space + size lock. `[BRAND]` **L**
14. **Add a price anchor / downloadable pricing guide** — gating price ×4 with zero anchor reads evasive, not exclusive. `[CRO+MARKET]` **M**
15. **Build ONE scroll-scrubbed image moment** — currently one FLIP-modal win, then motion silence. `[PORTFOLIO]` **L**
16. **Rebuild services off the square 4-card grid** (AI-reflex layout). `[BRAND+PORTFOLIO]` **M**
17. **Perf hygiene** — `defer` the 61KB parser-blocking `support.js`; preload Cormorant 600 + Mulish 400 woff2; delete unused `lulu-painting.jpg` (95KB). `[PERF]` **S**
18. **Copy fixes** — person flip (I → LuLu), "Speciality" → "Specialty" (US brand). `[COPY]` **S**

---

## Conflict map (Charles decides — the Chair does not rule)

- **Award craft vs. performance.** Portfolio wants a scroll-scrubbed image moment + real full-res photography; Perf needs total image weight near 150KB for green. Same asset pipeline — the trade-off is how much motion-heavy imagery ships before Lighthouse suffers.
- **Exclusivity vs. transparency.** Market/CRO want a published price anchor so it stops reading evasive; the premium-gating instinct wants price withheld. A positioning call.
- No other conflicts — seats disagree on priority, not direction.

**Chair's note:** every blocker is S/M — the site is one focused afternoon of plumbing away from being merely *unfinished* instead of *broken*.

---

## Raw seat verdicts

### PORTFOLIO / AWWWARDS — 59/100
A photographer's site with zero photographs where it counts — tasteful art direction, but static and mobile-broken; honorable-mention ceiling, not SOTD.
1. Portfolio shows NO photography — hero is CSS gradient, 6 gallery cells empty "drop photo" placeholders; caps every axis.
2. "SECTION 01" amateur tell everywhere — "(01) The heart behind the lens"…"(05) Let's begin" — strip them.
3. Mobile is stacked desktop — services/portfolio/process `repeat(N,1fr)` no mobile overrides; Process crushed unreadable.
4. Nav is decorative `<span>`s, no anchors/scroll — can't navigate.
5. One good motion moment (CTA→modal FLIP morph) then silence — no scroll craft.
**Must-fix:** load real photography into hero+gallery and build ONE scroll-scrubbed image moment.

### BRAND — 70/100
Ownable palette + warm body voice, undercut by an accent doing every job and a mark that survives nothing.
1. Champagne-gold #e6d6a8 has no assigned job — on CTAs, eyebrows, every stat number, numerals, bullet dots, focus rings; CTA stops pulling.
2. Mark is a fuzzy circular monogram-badge, illegible at 52px, won't survive 16px/reversed — #1 photographer-template tell.
3. Mark usage has no rule — 3 treatments (52/44/118px), no clear-space lock.
4. Voice split inverted — bio is craft ("barefoot chases," "belly laughs"), but generic hero headline sits biggest.
5. Services is the square 4-card grid (AI-reflex).
Wins: plum+gold less-traveled, stroked FOREVER, god-rays, FLIP modal. No Fraunces.
**Must-fix:** give champagne-gold ONE job (booking/action only).

### COPY — 78/100
Bio and section heads carry real voice; the most-visible line is the laziest cliché.
1. Hero "MEMORIES/captured/FOREVER" = #1 photographer cliché; pull from bio voice instead.
2. CTA vocabulary sprawls to 5 variants; cut to two; "Let's do a shoot!" clashes with unhurried brand.
3. Person flips first→third — form "I'll be in touch" vs success "LuLu will reach out."
4. Service cards adjective soup.
5. "Speciality" = British spelling on a US brand.
**Must-fix:** rewrite hero headline.

### SOCIAL — 18/100
Zero share infrastructure, no photo in shareable frame.
1. `<head>` is 2 meta tags — no title/description/og:image/twitter:card; link previews dead on arrival.
2. IG+Pinterest are non-clickable `<span>`, not links; only `<a>` is the modal mailto.
3. Share-frame has no photograph (CSS gradient hero).
4. Portfolio 6 empty placeholders — nothing to pin/repost.
5. No share system hook.
**Must-fix:** add real head (title, description, og:image = real photo, twitter card) + make IG/Pinterest real links.

### SEO — 22/100
Head effectively empty: no title/lang/description/h1/schema. Ships broken.
1. Missing `<title>` entirely — highest-weight tag.
2. No `<html lang>`, no meta description, no canonical, no OG.
3. Zero `<h1>` — visual headline is 3 styled divs; five h2 under no h1.
4. No Photographer/LocalBusiness JSON-LD.
5. Two portfolio slots alt="" (ok while placeholder).
**Must-fix:** add real `<title>` + `<html lang="en">` (60-second fix).

### CRO — 52/100
Clean CTA vocab + low-friction modal, but visible work + working inquiry pipe both absent.
1. Form reports success while sending nothing (setTimeout fakes "Request received") — 100% of inquiries vanish silently.
2. Empty portfolio kills desire before CTA.
3. Price+proof objections unanswered — "Inquire for pricing" ×4 no anchor; zero third-party social proof (honesty brand forbids fake — gather real).
4. Dead CTA zone across ~4 mid sections; "Inquire for pricing" spans not clickable.
5. No mobile sticky CTA, no analytics.
**Must-fix:** wire form to real endpoint (Formspree/Netlify) before deploy.

### MARKET — 43/100
Craft reads premium; words interchangeable with 10,000 photographers.
1. Fails only-you test — "soulful, unhurried, honest," "in-between moments" = shared category vocabulary.
2. Cliché headline costs Content points.
3. "Coastal California" (~840mi) signals nothing ownable — name a market.
4. No price anchor — gating price with zero anchor reads evasive not exclusive.
5. Single-path offer — one full form or nothing; no low-commitment capture.
**Must-fix:** replace category-generic promise with ONE claim only LuLu can make, pin headline to it.

### PERFORMANCE — 58/100
Green NOT achievable as-is; killers fixable/mechanical.
1. `lulu-portrait.png` = 2.33MB, 1024² PNG in ~530×480 box; WebP q80 ≈ 80-110KB; no lazy-load.
2. `lulu-logo.png` = 807KB, 1254² shown at 52/44/118px; WebP/SVG ≈ 15-30KB (25× oversized).
3. `support.js` 61KB synchronous in `<head>` — parser-blocking; add defer.
4. Google Fonts 13 files render-blocking, no preload; 132px LCP headline swaps metric-mismatched → CLS; preload Cormorant 600 + Mulish 400 woff2.
5. Unused `lulu-painting.jpg` 95KB ships — delete. Total image weight 3.14MB → achievable ~150KB.
**Must-fix:** recompress portrait+logo to display-sized WebP under NEW filename.

---

*Screenshots reviewed: desktop-full, mobile-full, modal-open (headless Chrome, 2026-07-06). Evidence pack retained in session scratchpad.*
