# PHASES.md — Web Brand Book Roadmap

One section per prompt. Screenshot → verify → gate → next. No bundling.

---

## STATUS

| Phase | Section | Status |
|---|---|---|
| 0 | Foundation docs | ✅ DONE |
| 1 | Element system (`assets/element-*.svg` — Raya's originals) | ✅ DONE |
| 2 | 01 — Hero | ✅ DONE (cinematic cream, 5 layered brand elements, RTL spine) |
| 3 | 02 — Brand Story | ✅ DONE (rebuilt — two-column REVEAL with bolt punctum + flowing beats, dropped 500vh scrub) |
| 4 | 03 — Brand DNA | ✅ DONE (5 pillar scenes) |
| 5 | 04 — Two Voices | ✅ DONE (split-column, center divider, parallax) |
| 6 | 05 — Colour System | ✅ DONE (6 full-bleed scenes) |
| 7 | 06 — Typography | ✅ DONE (bilingual specimen spread) |
| 8 | 07 — Elements Specimen | ✅ DONE (5-card grid) |
| 9 | 08 — Logo Variations | ✅ DONE (3-card RISE grid) |
| 10 | 09 — Logo Anatomy | ✅ DONE (DRAW callouts + 6 bilingual labels) |
| 11 | 10 — Clear Space | ✅ DONE (REVEAL diagram + 1x/2x/x legend) |
| 12 | 11 — Logo on Backgrounds | ✅ DONE (7 surfaces + rule card, hairline grid) |
| 13 | 12 — Logo Misuse | ✅ DONE (6-card grid + REVEAL X-mark stamps) |
| 14 | 13 — Applications | ✅ DONE (campaign hero + IG story + business card + letterhead) |
| 15 | 14 — Motion Demo | ✅ DONE (4 live CSS loop primitives) |
| 16 | 15 — Closing | ✅ DONE (yellow takeover, "لا نعيد سرد الدروس.. بل نصنع لحظة إدراك") |
| 17 | Motion v2 — Grand Opening + section punctum + RTL reveal | ✅ DONE |
| 18 | Copy rewrite — integrate copywriter's revised `COPY.md` | ✅ DONE — batch 2 complete. All 31 deltas applied: S02 beats 2–4 + foot; S03 dna-desc × 5 (Lato/LTR → Cairo/RTL); S04 voice-extra-ar × 2 added; S05 colour-story × 6 (Lato/LTR → Cairo/RTL); S06 Cairo H1; S09/S10/S12/S13/S14 `-en` headlines → Arabic with Cairo style; S11 bg-rule-ar + bg-headline-en/bg-rule-en → Arabic; S13 letterhead body; S14 mo-headline-ar; S15 cl-quote (8 spans → 6) + cl-sig-thanks-en → Arabic. |
| 19a | **Award-tier cinematic upgrade** — cursor, S03 vision, S15 stillness, S13 encounters | ✅ DONE (Session 4) |
| 19b | Element relevance + line-spacing audit (post-copy) | ✅ DONE (all §3b pairings correct; `.st-beat` 1.95, `.voice-quote-ar` 1.85, `.type-body` 1.85, `.art-lh-para` 1.9 — all long Arabic body text ≥ 1.85) |
| 20a | **Phase 19 — Brand-New ammunition** (15-icon construction set, الحرف letterform sub-spread in S06, brand-system overview as S03 Act 3, dead `.ap-hero/.ap-story/.ap-card-spec/.ap-letter` CSS removal) | ✅ DONE (Session 5) |
| 22 | **Session 6 — Award-eve emergency fixes** (S06 letterform spread DELETED — Cairo isn't the logo font; S13 photo-encounters → flat designed stationery using all 3 logo variants; S07 element-derived icons → 20-icon Service & UI library; S05 colour story copy verified; brand-palette cursor trail added) | ✅ DONE (Session 6, pre-submission) |
| 23 | **Session 7 — Post-submission polish** (S01 hero reverted A1 per user preference; S03 Act 2 — 5 DIFFERENTIATED pillar compositions (single-col centered / diagonal-thrust / rhythm-band / centered-with-ring / asymmetric-with-tick-ladder), resolves "one move repeated 5 times" knock; S03 Act 3 — system overview promoted to Vignelli-grade poster scale (120px ghost numerals, 88px Cairo 800 declarations, 280px label column); §13b Rules 17-19 codified) | ✅ DONE (Session 7) |
| 24 | **Session 8 — Mobile responsive sweep + Nano Banana prompt brief** (single `@media (max-width: 600px)` block at end of `<style>`; phone-specific hero composition with all 5 elements + logo scaled; chrome stacks 2-line; S07/S09/S11/S13 grid + label fixes; overflow-x guard; NANO-BANANA-PROMPTS.md authored with D1 still-life + D2 editorial-comic illustration + #5 cinematic illustrated hero; cultural framing PERMANENTLY banned per Session 4 + Session 8 user lock; CLAUDE.md §3f auto-invoke triggers locked; CLAUDE.md §13b Rule 20 mobile-sweep lessons codified) | ✅ DONE (Session 8) |
| 25 | Latin-paragraphs-in-RTL `dir="ltr"` HTML sweep (S04 / S11 / S13 / S15 — wraps Latin paragraphs to prevent bidi reorder at narrow widths per §13b Rule 12) | ✅ DONE (7 elements updated: S04 voice-name-en × 2 + voice-quote-en × 2, S11 bg-headline-en + bg-rule-en, S15 cl-sig-thanks-en) |
| 26 | Nano Banana 2 media generation + composite (D1 5× still-life, D2 5× illustration, #5 cinematic hero — blocked on user-generated images) | ⏸ BLOCKED ON USER |
| 27 | PDF export | later — separate phase |

---

## CURRENT PHASE — POLISH

All 15 sections built. Surgical polish ongoing.

### Polish completed (session 1)

- ✅ **S02 Brand Story** — full rebuild from 500vh scrub to clean 100vh two-column REVEAL (bolt punctum + flowing beats). Inline squiggle primitive removed, ghost "02" numeral removed.
- ✅ **S05 Colour System** — orange spark on orange field made visible via `filter: brightness(0) invert(1)` (white watermark). Other scenes untouched.
- ✅ **S06 Typography** — display specimen sizing reduced from 168px to clamp(56,6vw,96px) so text fits inside column. `overflow-wrap: break-word` safety. "168 / 900" labels updated to "96 / 900".
- ✅ **S09 Logo Anatomy** — rebuilt to use a centered SQUARE `.anat-frame` so logo, grid, dots share one coordinate space. Labels moved OUTSIDE the frame with leader hairlines so they never clip. Diagonal callout lines (which couldn't align across a non-square stage) replaced with anchor dots.
- ✅ **Chrome consistency** — every section counter wrapped in `dir="ltr"` so "13 / 15" no longer renders visually as "15 / 13" inside RTL context.
- ✅ **`?scrollTo=N`** URL param added as polish infrastructure (window scrolls to pixel N after load).

### Polish completed (session 2 — this session)

- ✅ **Chrome unify** — single canonical CSS block at end of `<style>` overrides 14 per-section chrome variants. All section headers identical: 11px Lato 4px uppercase + Cairo 13px medium Arabic chip + LTR-locked counter. No more drift.
- ✅ **S14 logo red-flag fix** — REVEAL primitive replaced typeset `<span>إدراك</span>` with `<img src="assets/logo-wordmark.svg">`. Closes the §3 rule violation that had survived two weeks of revisions.
- ✅ **S02 RTL flip + bolt bleed** — Arabic mission now anchors physical RIGHT (RTL leading); bolt punctum bleeds physical LEFT at 130% width. Beat line-height bumped to 1.95 per §7.
- ✅ **S13 Applications redesign** — hero campaign reads as a real OOH banner (pink full-bleed, arrows reduced to faded directional accent in corner). Letterhead has orange watermark spark + ink rule. Business card now 55×85 portrait aspect at equal grid width. IG story dropped flat-sticker dome for thin architectural outline + ink-dot apex. Grid columns equalised to `repeat(3, 1fr)` so no card balloons taller than its siblings.
- ✅ **Audit-mode + `?only=` URL flags** — reliable headless screenshot toolkit. Pre-flight verification finally repeatable.
- ✅ **Copy extraction** — every visible string in the book pulled into `COPY.md` with bilingual pairs, section anchors, and 🔒 LOCKED flags on Raya's words. Ready for copywriter.

### Motion v2 — Grand Opening + section punctum + RTL reveal (this session)

- ✅ **Grand Opening cinematic** — intro curtain holds the page until GSAP timeline starts (no element-popping pre-show). First-visit gating via `sessionStorage` so it plays once, not on every reload. Skip-intro button ("تخطي · Skip intro") top-left for repeat visits + accessibility. Brand-landed hairline draws under the logo as the final beat.
- ✅ **Section-entry punctum** — IntersectionObserver-driven yellow spark stamps at each section's RTL leading edge (top-right) on first entry. Single-shot per section, gated to `prefers-reduced-motion`. Hero, colour scenes, and closing exempted (they have their own brand presence). Misuse section uses ink-tone punctum.
- ✅ **RTL-native reveal** — `.reveal-rtl` utility class clips Arabic display in reading direction (right → left) with overshoot ease. Applied first to S02 mission line; ready to extend to all locked Arabic display strings.
- ✅ **Screenshot-mode safety** — every new motion gated with `?screenshot=true` bypass that pre-resolves to final state. Headless captures still work.

### Session 3 — Phase 18 batch 1 + S02 stabilization (this session)

- ✅ **Phase 18 — Copy rewrite, batch 1 integrated** — copywriter delivered revised `COPY.md`; 14 Arabic-only deltas applied surgically to `index.html` and mirrored in `COPY.md`. English untouched per user instruction. All 🔒 LOCKED phrases verified intact via grep. Founder name corrected `ريّا عبد الحي` → `راية عبد الحي` (S13 business card + S15 contact band). Full delta table in CLAUDE.md §13d.
- ✅ **S02 motion stabilization** — three bugs fixed at once: (a) GSAP `clipPath` `from()` on `.st-headline` was fighting the CSS `.reveal-rtl` class on the same element → headline stuck invisible. Removed the GSAP clip-path; (b) `.reveal-rtl` default-invisible CSS held the headline hostage when the IntersectionObserver didn't fire in live mode → removed `.reveal-rtl` class from `.st-headline`, replaced with simple GSAP RISE (`opacity:0, y:24`). Headline now visible by default with motion as decoration; (c) `.st-headline-en` had RTL bidi flipping the period to the wrong line when an inline Arabic word split the English sentence → added `dir="ltr"`.
- ✅ **Section punctum exemption extended to S02** — the universal `section[id]::after` yellow spark at top:36px / inset-inline-start:36px (= physical right in RTL) collided with S02's right-column eyebrow. Added `.s-brand-story::after { display: none; }` alongside the existing hero/colour/closing exemptions.
- ✅ **REVEAL-RTL primitive flagged experimental in DNA.md** — pattern requires inversion (opt-in clipping rather than opt-out) before re-applying to load-bearing content. Three new optimization rules locked in CLAUDE.md §13b (11, 12, 13).

### Session 4 — Award-tier cinematic upgrade (this session)

Target: **Awwwards Site of the Year** primary + **Brand New Awards** world-class secondary.
Think-tank panel (Bierut / Anton Repponen / Spiekermann / Tarek Atrissi / Villeneuve) converged on four moves landed in a 2-hour scope.

- ✅ **Custom brand-actor cursor** — yellow bolt 14×26px (inline SVG data-URI, fill `--c-yellow`) + halo ring with 12% lerp. Bolt lerps at 35% so it lags behind the mouse like a real object with mass. Brightens (`filter: drop-shadow + brightness`) near `a, button, [data-cursor=hot], summary, label[for], .nav-dot`. Hides on Arabic display headlines (`.st-headline, .cl-quote, .type-display, .type-h1, .type-h2, .dna-pillar-name, .hero-display, .ms-headline-ar, .cs-title-ar`) so type carries those moments uninterrupted. Touch devices get the auto cursor back. `prefers-reduced-motion` simplifies transitions.
- ✅ **S03 Act 1 — The Convergence** (new pinned cinematic scene, the Awwwards screen-record moment). Five vertical colour bars rise from the floor (staggered from edges-in), five elements (bolt/spark/arrows/dome/stairs) draw in above them with Arabic labels (اللحظة · الاندفاع · الطاقة · الوضوح · النمو), then converge toward physical centre as the logo SVG fades in as the unified mark with tagline "خمس قيم — هوية واحدة · Five values · one identity." ScrollTrigger pin + scrub 0.7, 140% scroll length. The existing 5 pillar scenes follow as **Act 2** (educational breakdown). Convergence math uses `getBoundingClientRect()` for the per-element distance to viewport centre — bulletproof against RTL flex reversal.
- ✅ **S15 stillness reveal** (Villeneuve's patience). Mic-drop quote split into 8 word-spans (`.cl-w`), revealing one-at-a-time with 0.55s stagger + blur-removal, ~5s total. Then **a 4-second silence** before the English subtitle, signature logo, and contact band emerge. The longest single beat in the book. Follows §13b Rule 11: words are default-visible in HTML, GSAP `from()` adds the entry as decoration. English subtitle gets `dir="ltr"` (§13b Rule 12 — fixes the trailing-period bidi flip).
- ✅ **S13 reframe — Applications → Encounters** (Tarek's reframe). Replaced the four flat mockups (campaign banner / IG story / business card / letterhead) with four photographic still-life "encounters." Each scene uses `background-image: url('assets/media/s13-0N.jpg')` so missing-image fallback is just cream (no broken-image icon). Logo composited as CSS-positioned `<img>` overlay on top of the blank paper in each photo — keeps the brand mark pixel-sharp and swappable. Yellow bolt punctum (`::after` data-URI) in the top-physical-left corner of each scene. Caption pills at bottom-physical-right (RTL leading edge). User-generated photos via Nano Banana 2 prompts (still-life, no people, business-grade editorial — Erik's discipline applied to Tarek's reframe).

**Session 4 post-build wrap-up** (after the 4 builds):
- ✅ **Images extracted from chat transcript.** User uploaded the 5 Nano-Banana WebPs inline in chat (not to disk). Wrote `qa/extract-images.ps1` — reads the tail of the session JSONL, regex-matches `"type":"image","source":{"type":"base64",…}`, writes the last N images to `assets/media/`. Output format: WebP (Nano Banana native), so HTML was switched from `.jpg` → `.webp` via a single targeted `replace_all` on the four S13 background-image URLs. **The technique is locked in CLAUDE.md §13c** under "Image extraction from chat (Session 4 trick)" — reusable.
- ✅ **Image order corrected.** Nano Banana uploads don't preserve order in the transcript; the brochure (the intended hero) extracted as slot 5, not 1. Renamed via PowerShell shuffle to put brochure → s13-01, desk → s13-02, card → s13-03, letterhead → s13-04, alt letter → s13-05.
- ✅ **Brochure logo composite repositioned.** First render put the logo on the LEFT page of the open spread — wrong reading direction. Flipped `inset-inline-end: 24%` → `inset-inline-start: 26%` so it sits on the right page (Arabic reading direction). Locked as CLAUDE.md §13b rule 14 step 5.
- ✅ **All four docs updated** (CLAUDE.md / DNA.md / PHASES.md / `qa/extract-images.ps1`) capturing this session's locks before compact.

**What was DEFERRED to next session** (out of 2-hour scope):
- 15-icon construction system (Brand-New-quality work — 3–4 hrs of design + integration)
- الحرف letterform sub-spread in S06 (embed inside S06 — do NOT break the 15-section frame)
- Motion video loops in hero / S03 / S15 (still-image discipline this round)
- Brand-system overview spread (needs icons + letterform first)
- Cleanup: orphaned `.ap-hero / .ap-story / .ap-card-spec / .ap-letter` CSS rules in `index.html` (S13 no longer uses them; remove in Phase 19 housekeeping)

**No user action required.** The 5 images are saved in `assets/media/`. Hard-reload (Ctrl+Shift+R) the index.html and the upgrade is live.

### Session 5 — Phase 19 Brand-New ammunition (this session)

Target: **Brand New Awards** secondary win (the system-pedagogy pages are where this jury scores). Parallel research → serial implementation pattern (user-chosen): three sub-agents proposed integration locations + composition, then implementation landed in sequence with screenshot gates per §11.

**A · Dead-CSS cleanup** ✅
337 lines of orphaned `.ap-hero / .ap-story / .ap-card-spec / .ap-letter` selectors (Session 4 had switched S13 to `.ap-scene` photo-composite but left the old CSS as dead code). Verified zero HTML references via grep before removal. Replaced with single marker comment.

**B · S06 letterform sub-spread** ✅
الحرف · The Letterform — embedded as third row strip below the existing two-column type spread, above the type-foot. 5 Cairo 900 letters (إ د ر ا ك in reading order, RTL flow) each carrying a `--h` CSS variable for `transform: scaleY()` per the **anatomically-correct letter-to-height map** (إ=78% · ا=70% · ك=62% · ر=52% · د=35%) — a Phase 19 disclosure addendum locked in DNA.md §3.1 to override the array-order assumption that contradicted letterform reality. Green stair element overlaid at 18% opacity as bottom-center construction-reveal watermark (small, atmospheric — not competing). Percentage tick row beneath the letters + bilingual museum-card caption ("Cairo's إدراك, measured. Type generates the system."). RISE on letters (stagger 80ms) + DRAW on stair watermark on delay. Counter stays `06 / 15`. Section grows past 100vh.

**C · 15-icon construction system as S07 Act 2** ✅
The Brand-New jury hook. 5 families × 3 inline-SVG icons each, single-stroke 3u-secondary on 24u artboard. Each icon visually derives from its parent element-*.svg silhouette. Names locked: stairs/growth (الخطوة step / المسار path / الإنجاز milestone), arrows/energy (المتابعة next / الإرسال submit / المحاولة retry), bolt/moment (التنبيه alert / السرعة quick / **الإدراك insight ★ money shot**), dome/clarity (الإجابة answer / الحماية safe-space / التركيز focus), spark/drive (الفكرة idea / الانطلاق ignite / الاتصال contact). Per-row layout (RTL): 3 icons flowing physical right-to-left + family label cell at row-end carrying parent element thumbnail + colored inline-start rule (= inner edge facing the icons in RTL) + bilingual name + story. Construction-grid dot backdrop (8% ink) behind each icon-art. Money-shot bolt insight icon = polyline `(18,4) → (10,11) → (15,13) → (6,21)` — the brand-thesis kick at the middle vertex. Per-stroke DRAW via `stroke-dasharray` computed by JS `getTotalLength()`, then GSAP animates `stroke-dashoffset → 0` (0.9s, 180ms inter-cell stagger). Filled dots fade in last. Family label RISE last per row. S07 now 2-act, counter stays `07 / 15`.

**D · Brand-system overview as S03 Act 3** ✅
Vignelli-style index poster appended as the third act of S03. Per §13b Rule 16 multi-act pattern. Five horizontal bands stacked on a master baseline grid:
1. **اللون · COLOUR** — 5 colour chips with hex + Arabic story-word (اللحظة · الاندفاع · الطاقة · الوضوح · النمو) + English caption + colored rule
2. **العنصر · ELEMENT** — 5 parent `element-*.svg` thumbs aligned column-for-column to the colour band above
3. **الأيقونة · ICON · 15** — 5 cells each carrying 3 micro-icons (28×28), grouped by colour family
4. **الخط · TYPE** — 2-column split: "إدراك" Cairo 900 right / "Idrak" Lato 700 left
5. **الحركة · MOTION** — 4 cells: REVEAL (yellow box clip-path), RISE (pink box translate), DRAW (blue polyline stroke-dash), EASING (cubic-bezier curve SVG)

Each band has a label cell on physical-LEFT (band number 01/05–05/05 + Arabic name + English name) and a 5-cell body grid. Column alignment between Bands 1-2-3 (colour → element → icon, same 5-column rhythm) is the Awwwards screen-record beat — the brand declaring "look how aligned we are." Sequential REVEAL stack via GSAP `from()` (180ms stagger, opacity + y:24, ~1.4s total assembly). Per §13b Rule 11: bands default-visible, motion adds entry decoration only. Counter stays `03 / 15` — S03 now three acts under one section number.

**Session 5 infrastructure additions:**
- ✅ **`?act=N` URL flag** added to screenshot-mode bypass — hides everything in S03 except the requested act (1=CONVERGE, 2=pillars, 3=overview) so headless can isolate any single act. Useful for S03 verification because `?only=s03` blows .dna-vision to 100vh = window-height in tall captures. Now `?screenshot=true&only=s03&act=3` cleanly captures just the system overview.
- ✅ **DNA.md §3.1 letter-to-height map locked** — anatomically correct mapping (إ=78 · ا=70 · ك=62 · ر=52 · د=35) overrides the array-index assumption. One-line addendum explains the disclosure rationale.
- ✅ **All 3 docs updated** (CLAUDE.md §12 / DNA.md §5 / PHASES.md status table) before compact.

**What was DEFERRED again** (still out of session scope):
- Motion video loops in hero / S03 / S15 (still-image discipline)
- Mobile responsive sweep (Phase 20b backlog)
- PDF export (Phase 21)

### Upcoming — Phase 18 batch 2 (next session)

**Remaining copy-rewrite work** (when copywriter returns next batch)
1. Decide on long-Arabic-replacing-short-chip cases (S10 legend, S11 rule card) — needs layout pass
2. Decide on S03–S07 Arabic-only descriptions (new draft removes English; conflicts with "keep English" rule)
3. Surgical replace in `index.html` — touch nothing else
4. Re-screenshot every affected section
5. Verify: display headlines don't overflow narrow columns, Arabic line-spacing ≥ 1.85, RTL anchoring intact, 🔒 LOCKED Raya phrases unchanged

### Backlog after copy

1. **Element relevance audit** — verify every section's brand element matches its color story per §3b pairings
2. **Mobile responsive sweep** — 375 and 768 breakpoints
3. **Extend `.reveal-rtl` to remaining Arabic display strings** (S03 pillar names, S04 voice names, S05 colour names, S06 type specimen, S15 mic-drop)
4. **Optional motion picks from "ideas list"** — cursor as brand actor, flip counter, colour-mood snap transitions, S03 horizontal camera track, magnetic elements, answer-dot heartbeat
5. **Performance pass** — Lighthouse + bundle audit
6. **PDF export** — final phase, separate setup

---

## Per-Section Checklist (run before reporting done)

1. Build section in `index.html`
2. Screenshot: `--window-size=1440,900` for above-fold, `--window-size=1440,15000` for full doc
3. Read screenshot — if it looks like a template, rebuild
4. Verify: dominant colour correct? Motion wired? Bilingual pair present? Logo untouched?
5. Report result. Stop. Wait for gate.

**Full-doc screenshot command:**
```powershell
& "C:\Program Files\Google\Chrome\Application\chrome.exe" --headless --disable-gpu --hide-scrollbars --virtual-time-budget=8000 --screenshot="C:\Projects\Idrak-Brand-System\qa\all-pages.png" --window-size=1440,15000 "file:///C:/Projects/Idrak-Brand-System/index.html?screenshot=true"
```

**Per-section command (single section above-fold):**
```powershell
& "C:\Program Files\Google\Chrome\Application\chrome.exe" --headless --disable-gpu --hide-scrollbars --virtual-time-budget=8000 --screenshot="C:\Projects\Idrak-Brand-System\qa\sNN.png" --window-size=1440,900 "file:///C:/Projects/Idrak-Brand-System/index.html?screenshot=true#sNN"
```

---

## Absolute Rules (every phase)
- Logo: always `<img>` — never traced, never recreated
- Elements: only `assets/element-*.svg` (Raya's originals) — `sys-*` deprecated
- Colours: only `:root` tokens — no hard-coded hex
- Fonts: Cairo + Lato only
- Motion: all gated to `body.live`
- Copy: Raya's words from CLAUDE.md §10 — no fabrication
- RTL is the master axis — anchor brand identity to the physical right
