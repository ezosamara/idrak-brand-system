# DNA.md — Compositional Grammar

**Source discipline:** SBF brand book structure. **Application:** إدراك web brand book.
**Purpose:** Rules for how this brand speaks visually — not what it looks like, how it *moves*.

---

## 1. STRUCTURAL GRAMMAR (borrowed from SBF)

### 1.1 Bilingual discipline
- Every section has a **topic chip**: Arabic title over English title, both prominent.
- Body copy: **two synchronized columns** — Arabic right, English left. Same paragraph count.
- Section number as **giant numeral** — spatial anchor, not decoration.

### 1.2 Specimen-grid logic
- Educational sections (Logo, Colour, Type, Elements) presented as **labelled specimen grids**.
- Each cell isolated, generous interior padding. Elements as artifacts, never as glue.

### 1.3 White-space rhythm
- ~45% of each section viewport blank. Breathing room is the design.
- Inter-block spacing: multiples of 8px (8 / 16 / 24 / 40 / 64 / 96).

### 1.4 Section furniture (web version)
- Sticky mini-nav: `Brand Identity · دليل الهوية` left + section counter right — `01 / 15` format.
- No print marks. No running headers as text blocks. Web chrome is minimal.

### 1.5 Tone
- **Clinical, not decorative.** Captions like museum cards. Arabic: formal MSA. English: concise.
- Demonstration over description. Every rule has a live specimen, not an explanation of a specimen.

---

## 2. WEB LAYER (إدراك adds, SBF had none)

- **Cinematic scroll:** GSAP ScrollTrigger scrub + pin for narrative sections.
- **Motion as meaning:** each element animates in a way that mirrors its colour story (DRAW = growth, BURST = discovery, RISE = momentum).
- **Parallax depth:** background elements travel at 0.3–0.6× scroll speed vs. foreground.
- **Mouse parallax:** 2–4px offset on hero — the brand has depth.
- **Full-viewport colour washes:** Colour section — each colour takes over the entire screen.

---

## 3. إدراك ELEMENT SYSTEM

### 3.1 Geometry rules
| Token | Value |
|---|---|
| Base unit (u) | 8px |
| Stroke weight | 6u (48px) primary / 3u (24px) secondary |
| Corner radius | ≤ 1.5u (12px) |
| Artboard | 24u (192px) square |
| Stair heights | 35% / 52% / 78% / 62% / 70% of letterform |

**Letter-to-height map (locked May 2026 — anatomy, not array order):**
| Letter | Height | Why |
|---|---|---|
| **إ** | **78%** | Tallest — alif + hamza |
| **ا** | **70%** | Cap-height alif (no hamza extension) |
| **ك** | **62%** | Bowl + kashida flourish |
| **ر** | **52%** | Bowl above baseline, no ascender |
| **د** | **35%** | Squat dal, baseline-bound |

The percentages set the height *array* `[35, 52, 78, 62, 70]` for the green stair element. The letter→height assignment above governs the S06 letterform sub-spread — assigning by anatomy, not by array index. Without this disclosure the brand book would render إ as the shortest letter, which contradicts visible letterform reality. Anchored explicitly here so future implementations don't accidentally re-invert the mapping.

Source geometry: إدراك letterform profile. Redrawn forms inspired by `incoming/*.svg` mood are allowed — never drop-in raw.

### 3.2 Element family (10 pieces — locked in `assets/system/`)
1. **STEP** — staircase, echoes إ-د-ر-ا-ك letter heights. Meaning: the learning journey.
2. **BURST** — 6 rays, 12° spread, all 5 colours. Meaning: the إدراك moment, discovery.
3. **ARC** — quarter-arc, 6u stroke. Meaning: the turn toward clarity.
4. **CHEVRON** — triple RTL chevron. Meaning: direction, forward motion.
5. **SQUIGGLE** — 3-period sine. Meaning: the irregular path, neurodiversity.
6. **HALF-CIRCLE** — solid filled. Meaning: the answer, completeness.
7. **TRIANGLE** — equilateral outline. Meaning: foundation, three pillars.
8. **SPARK** — 4-way cross. Meaning: the moment of contact, ignition.
9. **BOLT** — angular zigzag. Meaning: energy, the fast learner.
10. **X-MARK** — thick crossed strokes. Meaning: prohibition (Misuse section only).

### 3.3 Colour assignment
- ≤1 brand colour per element (BURST: all 5).
- Match element to its section's dominant colour (see CLAUDE.md §6).

### 3.4 Motion language
All gated to `body.live`. Easing throughout: `cubic-bezier(0.16, 1, 0.3, 1)`.

| Primitive | CSS / JS | Duration | When |
|---|---|---|---|
| REVEAL | `clip-path: inset(100% 0 0 0)` → `inset(0)` | 0.6–0.9s | Headlines (Latin), logo |
| REVEAL-RTL ⚠️ experimental | `clip-path: inset(0 0 0 100%)` → `inset(0)` | 0.9s w/ 5% overshoot | Arabic display — reveals in reading direction (right→left). **DO NOT apply to load-bearing content** (see CLAUDE.md §13b rule 11). The default-clipped CSS state held the S02 mission line hostage when the IntersectionObserver didn't fire reliably. Reserved for non-critical decoration until the pattern is rewritten as opt-in (`.is-rtl-clipped` applied by JS, then removed) rather than opt-out. |
| RISE | `translateY(40px) opacity:0` → `0 / 1` | 0.4–0.6s | Cards, body, captions |
| DRAW | `stroke-dashoffset` → 0 | 0.8–1.2s | SVG elements (inline only) |
| SCRUB | GSAP pin + scrub | scroll-driven | Brand story, DNA section |
| PARALLAX | `y` at 0.3–0.6× scrub rate | scroll-driven | Background elements |
| LOOP | CSS keyframe, infinite | 2–4s cycle | Hero burst only |
| PUNCTUM | yellow spark stamps via IntersectionObserver | 1.4s, single-shot | Every section's RTL leading edge on first entry |
| CURTAIN | full-bleed cream overlay → opacity 0 | 0.5s | Holds the page until Grand Opening starts (first visit only) |
| LANDED | scaleX(0)→1 on a 64px hairline under logo | 0.8s | Final beat of the entrance — "brand has arrived" |
| CONVERGE | ScrollTrigger pin + scrub 0.7, 140% scroll length; bars grow + elements appear + converge to viewport-centre + logo crown fades in | scroll-driven | S03 Act 1 only — the Awwwards screen-record beat. Per-element `x` distance computed via `getBoundingClientRect()` to viewport centre so it works regardless of RTL flex reversal. |
| STILLNESS | word-spans (`.cl-w`) opacity+y+blur stagger 0.55s, then deliberate 4-second hold before downstream elements emerge | ~10s total | S15 closing only. Villeneuve's counter to high-motion sections. Words default-visible (§13b rule 11), GSAP `from()` adds entry as decoration. |
| CURSOR-BOLT | yellow bolt SVG (data-URI fill `#F5D03A`) + halo ring lerp-following at 35% / 12%; brightens via filter on `a, button, [data-cursor=hot]`; hides on Arabic display headlines | continuous | Every page. The brand actor on the canvas. Touch-device fallback (`@media (hover:none)`) restores auto cursor. |

Hover: 4px lift (`translateY(-4px)`), 0.2s ease. Never scale. Never rotate.

### Motion philosophy
Every animation must answer: *does this make the closed door more clearly open?* (the brand thesis, CLAUDE.md §3c). If "no, but it's pretty" — banned. Decorative animations make a brand look insecure.

### First-visit gates
Any cinematic > 1.5s gets a `sessionStorage` flag so it plays once. Big intros are precious. Pair with a skip control + `prefers-reduced-motion` guard.

### RTL-native motion
Western motion conventions clip from the bottom or fade from below. Arabic display in this brand reveals in **reading direction** — right to left (REVEAL-RTL). This single move signals authentic Arabic-first authorship.

**Status (May 2026):** the REVEAL-RTL primitive is currently disabled on critical content because its default-clipped CSS state proved fragile in live mode (§13b rule 11). Re-introduction requires inverting the default — content visible unless JS explicitly marks it for clipping. Until that rewrite, S02 mission uses a simple GSAP RISE instead.

---

## 4. ANTI-PATTERNS

- ❌ Static motion storyboards (FRAME 1 / FRAME 2 / FRAME 3 boxes — banned forever)
- ❌ Drop shadows, blur, gradients, glassmorphism
- ❌ A4 page dimensions or print constraints in web sections
- ❌ Centered-stack hero layouts (template look)
- ❌ Tashkeel on Arabic body
- ❌ Raw drop-in of `incoming/*.svg`
- ❌ All 5 colours on one section
- ❌ `#FFFFFF` anywhere — use `--c-bg` or `--c-bg-dark`

---

## 5. SECTION MAP

| # | Section | SBF analogue | Motion primitive | DNA notes |
|---|---|---|---|---|
| 01 | Hero | p1 | REVEAL + LOOP | Dark, logo draws, display REVEALS massive |
| 02 | Brand Story | — | REVEAL + RISE | Two-column scene. LEFT: bolt punctum + caption. RIGHT: mission headline (clip-path REVEAL) + flowing narrative beats (staggered RISE). SCRUB primitive was tried (500vh pin) but readability suffered — replaced with the consistent REVEAL+RISE pattern used across the book. |
| 03 | Brand DNA | p4 | **CONVERGE (Act 1)** + DRAW + RISE (Act 2) + INDEX-REVEAL (Act 3) | Three-act section (Phase 19 added Act 3). Act 1 = pinned cinematic CONVERGE — five colour bars rise + elements converge to centre + logo crown emerges (Awwwards screen-record moment). Act 2 = five pillar breakdowns. **Act 3 — Vignelli-style system overview**: five horizontal bands (COLOUR / ELEMENT / ICON / TYPE / MOTION) stacked on a master baseline grid. Sequential REVEAL stack with 180ms stagger. Column alignment between Bands 1-2-3 proves the §3b colour-element-icon spine in one glance. The "system poster" beat — counterweight to Act 1's cinema, Act 2's pedagogy. |
| 04 | Two Voices | p10 | PARALLAX | Arabic right / English left, colour-split |
| 05 | Colour System | p9 | full-viewport wash | Scroll through each colour as a scene |
| 06 | Typography | p10 | REVEAL + DRAW (Phase 19) | Two-act. Act 1 = bilingual specimen spread. Act 2 = الحرف letterform sub-spread showing how إ-د-ر-ا-ك letterforms generate the stair element's 5 heights (anatomical map: إ=78 · ا=70 · ك=62 · ر=52 · د=35, locked §3.1). Cairo 900 letters on shared baseline + green stair watermark + percentage ticks + bilingual museum-card caption. RISE on letters + DRAW on stair. |
| 07 | Elements | — | DRAW + STROKE-DASH (Phase 19) | Two-act. Act 1 = existing 5-card grid showing the parent elements. Act 2 = 15-icon construction system (5 families × 3 icons each, single-stroke 3u on 24u artboard, each icon derived from its parent element's silhouette). Per-row layout: 3 icons + family label cell on RTL trailing edge. Per-icon DRAW via `stroke-dasharray` + GSAP. Money-shot icon = #7 الإدراك (bolt) — DRAW timing encodes the brand thesis. |
| 08 | Logo Variations | p3 | RISE | 3-up grid, dark/light/colour versions |
| 09 | Logo Anatomy | p4 | DRAW | Callout lines draw in |
| 10 | Clear Space | p5 | REVEAL | x-height diagram reveals |
| 11 | Logo on Backgrounds | p7 | RISE | Grid: ink/cream/each colour |
| 12 | Logo Misuse | p8 | REVEAL | X-marks stamp over wrong versions |
| 13 | Applications → **Encounters** | p13 | RISE + clipPath REVEAL on hero | Photographic still-life scenes (`assets/media/s13-0N.webp`) as `background-image` on `.ap-scene` + logo SVG composited as absolute `<img>` overlay on blank paper. No flat mockups. Yellow bolt punctum `::after` data-URI top-physical-left. Captions bottom-physical-right (RTL leading). Session-4 reframe per Tarek. |
| 14 | Motion Demo | — | LOOP | Live animation specimens |
| 15 | Closing | p14 | **STILLNESS** (Session 4) | Mic-drop word-span reveal + 4-second silence + late signature/contact stagger. Patience as design decision — counter-balances S03's maximalism. The cursor steps aside on `.cl-quote` so the type carries this beat. |
