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
2. **BURST** — 5 rays, one per pillar, all 5 brand colours. **The primary brand signature mark.** Meaning: the إدراك moment — the unification of all five values into one form. It is the only element that legitimately uses all five colours simultaneously, because it IS the brand system made visible. Appears at the top of `logo-with-rays.svg`, as the custom cursor, as the hero floating element, as the S02 punctum figure, as the S07 culminating panel, and as the S03 Act 1 convergence crown.
3. **ARC** — quarter-arc, 6u stroke. Meaning: the turn toward clarity.
4. **CHEVRON** — triple RTL chevron. Meaning: direction, forward motion.
5. **SQUIGGLE** — 3-period sine. Meaning: the irregular path, neurodiversity.
6. **HALF-CIRCLE** — solid filled. Meaning: the answer, completeness.
7. **TRIANGLE** — equilateral outline. Meaning: foundation, three pillars.
8. **SPARK** — 4-way cross. Meaning: the moment of contact, ignition.
9. **BOLT** — angular zigzag. Meaning: energy, the fast learner. Pillar 1 element (اللحظة / yellow). Appears as S15 background silhouette.
10. **X-MARK** — thick crossed strokes. Meaning: prohibition (Misuse section only).

### 3.3 Colour assignment
- ≤1 brand colour per element (BURST exception: all 5, one per ray).
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
| CONVERGE | ScrollTrigger pin + scrub 0.7, 140% scroll length; bars grow + elements appear + converge to viewport-centre + burst crown fades in | scroll-driven | S03 Act 1 only — the Awwwards screen-record beat. Per-element `x` distance computed via `getBoundingClientRect()` to viewport centre so it works regardless of RTL flex reversal. |
| STILLNESS | word-spans (`.cl-w`) opacity+y+blur stagger 0.55s, then deliberate 4-second hold before downstream elements emerge | ~10s total | S15 closing only. Villeneuve's counter to high-motion sections. Words default-visible (§13b rule 11), GSAP `from()` adds entry as decoration. |
| CURSOR-BURST | `element-rays-burst.svg` as CSS `background-image` at 28×28px + halo ring lerp-following at 35% / 12%; brightens via filter on `a, button, [data-cursor=hot]`; hides on Arabic display headlines (`.st-headline, .cl-quote, .type-display, .type-h1, .type-h2, .dna-pillar-name, .hero-display, .ms-headline-ar, .cs-title-ar`) so type carries those moments uninterrupted. Touch-device fallback (`@media (hover:none)`) restores auto cursor. | continuous | Every page. The brand actor on the canvas — the signature mark following the user's hand. |

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
- ❌ All 5 colours on one section (burst is the sole exception — it IS the system)
- ❌ `#FFFFFF` anywhere — use `--c-bg` or `--c-bg-dark`
- ❌ Banning `element-rays-burst.svg` — it is the primary brand signature mark, never an anti-pattern

---

## 5. SECTION MAP

| # | Section | SBF analogue | Motion primitive | DNA notes |
|---|---|---|---|---|
| 01 | Hero | p1 | REVEAL + LOOP | Cream, logo draws, display REVEALS massive. `logo-with-rays.svg` is the RTL protagonist. `element-rays-burst.svg` is the hero floating element. Brand video (`nanno-brand-video.mp4`) as background at 0.08 opacity, `mix-blend-mode: multiply`. |
| 02 | Brand Story | — | REVEAL + RISE | Two-column scene. LEFT: `element-rays-burst.svg` as punctum figure + "اللحظة · The moment" caption. RIGHT: eyebrow + mission headline (clip-path REVEAL) + flowing narrative beats (staggered RISE). SCRUB primitive was tried (500vh pin) but readability suffered — replaced with the consistent REVEAL+RISE pattern used across the book. |
| 03 | Brand DNA | p4 | **CONVERGE (Act 1)** + DRAW + RISE (Act 2) + INDEX-REVEAL (Act 3) | Three-act section. **Act 1** = pinned cinematic CONVERGE — five colour bars rise + elements converge to centre + `element-rays-burst.svg` crown emerges (Awwwards screen-record moment). **Act 2** = five DIFFERENTIATED pillar breakdowns (CLAUDE.md §13b Rule 17). **Act 3 — Vignelli-style editorial index**: five horizontal bands (COLOUR / ELEMENT / ICON / TYPE / MOTION). Band label is editorial-counter style — band number at 10px / letter-spacing 3px / opacity 0.4; Arabic band name at clamp(28px,3vw,40px); label column 200px. This is a quiet index, not a display-type poster — the "120px ghost numeral / 88px Cairo 800" era was a bug, now fixed (CLAUDE.md §13b Rule 21). Act 3 bottom carries a 3-image triptych (`idrak-new-01/02/03.jpg`). Chrome reads `Brand DNA · The System · Index`. |
| 04 | Two Voices | p10 | PARALLAX | Arabic right / English left, colour-split |
| 05 | Colour System | p9 | full-viewport wash | Scroll through each colour as a scene |
| 06 | Typography | p10 | REVEAL + DRAW (Phase 19) | Two-act. Act 1 = bilingual specimen spread. Act 2 = الحرف letterform sub-spread showing how إ-د-ر-ا-ك letterforms generate the stair element's 5 heights (anatomical map: إ=78 · ا=70 · ك=62 · ر=52 · د=35, locked §3.1). Cairo 900 letters on shared baseline + green stair watermark + percentage ticks + bilingual museum-card caption. RISE on letters + DRAW on stair. |
| 07 | Elements | — | DRAW + STROKE-DASH + RISE | **Act 1** = 5-card grid showing the parent elements. **Act 2** = 20-icon Service & UI library (Session 6): 3 functional groups (Services / Audience & Contact / UI Utility), single-stroke 24×24 viewBox. **`elements-master` burst/signature block** is at the END of S07 — after the icons, before the footer. Reads as culmination: five sub-elements → their derived icons → the unifying burst. Placement is intentional and locked. |
| 08 | Logo Variations | p3 | RISE | 3-up grid, dark/light/colour versions |
| 09 | Logo Anatomy | p4 | DRAW | Callout lines draw in |
| 10 | Clear Space | p5 | REVEAL | x-height diagram reveals |
| 11 | Logo on Backgrounds | p7 | RISE | Grid: ink/cream/each colour |
| 12 | Logo Misuse | p8 | REVEAL | X-marks stamp over wrong versions |
| 13 | Applications | p13 | RISE + clipPath REVEAL | **Business cards**: `assets/card-front.svg` + `assets/card-back.svg` (Raya's actual designed SVG cards). **Nanno illustration band** (5-cell): `nanno-student-desk.png`, `nanno-notebook-writing.jpg`, `nanno-boy-window.png`, `nanno-father-son.png`, `nanno-parent-girl.png`. **Brand photography triptych band** (`ap-photo-band`): 3-column asymmetric grid (1 / 1.6 / 1) with `idrak-new-01/02/03.jpg`, dark gradient overlay, LTR labels. S13 stationery photographic still-life scenes (`assets/media/s13-0N.webp`) also present for letterhead context. |
| 14 | Motion Demo | — | LOOP | Live animation specimens |
| 15 | Closing | p14 | **STILLNESS** (Session 4) | Yellow takeover. Mic-drop word-span reveal + 4-second silence + late signature/contact stagger. The cursor (`.cursor-burst`) steps aside on `.cl-quote` so the type carries this beat. **`cl-quote` line-height: 1.15** (was 0.95 — Arabic lines collided; fixed Session 9). **Ezo Studio credit** (`.cl-studio`) at the very bottom: `Brand identity work by · EZO STUDIO · 2026` — 10px / 3px letter-spacing / uppercase / centered / 55% opacity. |
