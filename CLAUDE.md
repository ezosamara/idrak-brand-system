# CLAUDE.md — Idrak Brand System

Project rules. Read every session. Non-negotiable.
Companion docs: `DNA.md` (grammar) · `PHASES.md` (roadmap)

---

## 1. PROJECT IDENTITY
- **Client:** Raya Abd Alhay · **Brand:** إدراك — Smart Learning Center. Tira.
- **Deliverable:** Web brand book (`index.html`). Cinematic scroll experience. PDF later.
- **Quality bar:** D&AD / Brand New / Awwwards level. Art-directed, not generated.

## 2. LANGUAGE — ABSOLUTE
- Rendered content: **Arabic + paired English** on every educational section.
- English standalone: tagline, eyebrow labels, captions, dimension callouts only.
- Code and reports: English. Missing copy = `[يملأ من ريا]`. Never fabricate.

## 3. ANTI-FABRICATION — ABSOLUTE
- Zero invented numbers, stats, quotes, awards, dates.
- Zero invented brand copy. Missing copy = `[يملأ من ريا]`. Never fabricate definitions, taglines, or descriptors.
- **Logo always = `<img src="assets/logo-*.svg">`. Never trace or recreate.**
- White logo: `filter: brightness(0) invert(1)` CSS only. No new SVG file.

## 3b. HARD DESIGN RULES — LOCKED, NON-NEGOTIABLE
- **No black backgrounds.** `--c-bg-dark` is banned from full-section backgrounds. It exists only for micro-accents (cursor dot, single-pixel rules, type on cream). Section backgrounds use `--c-bg` (cream) or one of the 5 brand colors at a meaningful moment (Colour System section's full-takeover scenes).
- **The brand vocabulary lives in `assets/element-*.svg`** — Raya's original brand-drawn shapes with 3D layered geometry, drop-shadow craft, and dimensional depth. These are NOT "deprecated." They are the primary visual system. The `sys-*` redraws were too sterile and are deprecated in their favor.
- **Each brand color is paired with one specific element by story** (the brand grammar — do not improvise pairings):

  | Color | Element file | Brand story |
  |---|---|---|
  | `--c-green` | `element-stairs-green-new.svg` | The learning journey — the climb |
  | `--c-pink` | `element-arrows-pink-new.svg` | Forward motion, the push toward the moment |
  | `--c-yellow` | `element-bolt-yellow-new.svg` | Lightning of understanding — the إدراك moment |
  | `--c-blue` | `element-semicircle-blue.svg` | Clarity, the dome of the answer |
  | `--c-orange` | `element-spark-orange.svg` | Ignition, the moment of contact |

- **Reserve vocabulary** (use only when their specific meaning is needed): `element-banner-ribbons.svg` (celebration / achievement), `element-squiggle-yellow.svg` (the irregular path — alt for bolt). `element-bolt-yellow-new.svg` and `element-squiggle-yellow.svg` both belong to yellow; pick the one that matches the section's moment.
- **Banned outright:** `element-rays-burst.svg` (rainbow fan, childish), `element-x-orange.svg` (Misuse section only), `element-arc-purple.svg` (purple is not in the palette), `element-triangle-orange.svg` and `element-spark-blue.svg` (redundant with the locked pairings above).
- **The `sys-*` redrawn elements are deprecated** in favor of the originals. They will not appear in any section.
- **Always render elements as `<img src="assets/element-*.svg">`** — never trace, never recreate. Same rule as the logo: the SVG file is sacred.
- **No ink/black inside elements.** Elements carry only their assigned brand color.
- **Vibrancy comes from amplifying color presence**, not multiplying decorative instances. Big confident shapes covering 30–50% of the canvas beat ten tiny accents every time.
- **Logo-first, then type.** The `assets/logo-wordmark.svg` file is the primary visual identity. Cairo display type is secondary and **never duplicates the brand name `إدراك`** at display scale — that would be recreating the logo in CSS, which §3 forbids. Type carries content (headlines, body, captions). The logo carries identity.

## 3c. ART-DIRECTION THESIS — LOCKED

**إدراك is the moment a closed door opens.**

The book is composed AROUND that moment, not around the brand name. Every section captures one moment of perception — staged in depth, with our brand elements as the layered set. Cream is the air the moment moves through. The logo SVG is the brand entering the page.

**Four visual implications — every section must obey:**

1. **Cream is the base, depth is required.** `--c-bg` cream is the default field. Cream-flat is banned. Every cream page carries **2+ layers of brand-element depth** (SQUIGGLE / ARC / HALF-CIRCLE / single BURST ray) at varied scales and z-translations, plus at least one brand-color punctum. Brand-color full-takeovers are reserved for the Colour System section.
2. **RTL is the master axis.** Arabic reads right-to-left → editorial anchors live on the **physical right** (spine, primary entry point, logo). Folio numeral and trailing chrome live on the **physical left**. Centered-symmetric layouts are banned.
3. **The logo SVG is sacred AND prominent.** Always `<img src="assets/logo-*.svg">`, never typeset. The hero shows the actual SVG at massive scale. No display-type duplication of the brand word anywhere in the book.
4. **Bilingual is a design tension, not a translation chore.** Arabic and English overlap, run as vertical spines, drown each other. Never default to parallel left-right columns.

## 3d. CINEMATIC — DEFINITION (LOCKED)

"Cinematic" for this project means one specific thing, not a vibe.

- **Layered depth, not flat.** Every composition has 2–4 visual layers separated on the z-axis via `transform-style: preserve-3d` + `translateZ()`. Background SVGs sit furthest back, brand chrome closest.
- **Scripted reveals, never all-at-once.** Elements enter on their own timing (100–300ms stagger). Page-load is a choreographed sequence: field → background layers → logo → editorial chrome → punctum.
- **Differentiated parallax per layer.** Scroll-driven motion at varied speeds: background 0.2–0.4×, midground 0.5–0.7×, foreground 1.0×. Creates depth-of-field illusion without Three.js.
- **3D micro-rotation on mouse.** Passive layers respond via CSS `perspective` + `rotateX/Y` (max ±4°). Never scale, never spin.
- **Camera language for narratives.** ScrollTrigger pin + scrub = a "tracking shot" through long sections.
- **NOT cinematic:** autoplay video, particle systems, Three.js volumetric scenes, lens flares, glow, blur, gradients, hover-bounce micro-interactions, looping decorative spinners.

## 3e. SESSION STARTUP — REQUIRED SKILLS

Before any design work on this project, invoke in order:
1. `using-superpowers` (always first)
2. `frontend-design`
3. `3d-web-experience`
4. `scroll-experience`

If any skill applies even at 1% confidence, invoke it before responding.

## 3f. AUTO-INVOKE TRIGGERS — SKILLS & AGENTS (LOCKED)

**The user will NOT manually request skills or agents. Invoke them automatically based on the trigger table below.** This rule overrides any default reluctance — Idrak is a design-award submission, the bar is "Awwwards Site of the Year + Brand New Awards," and every relevant skill must fire without prompting.

### Skills — auto-invoke on these triggers

| If the work involves... | Auto-invoke skill |
|---|---|
| Session start (always, every session) | `using-superpowers` → `frontend-design` → `3d-web-experience` → `scroll-experience` |
| Typography pass (sizing, pairing, specimen, Cairo/Lato decisions) | `wondelai-web-typography` |
| Motion / animation / cursor / GSAP work | `motion-advanced` + `motion-canvas` (for cursor trail / canvas particle work) |
| Before claiming any section DONE | `wondelai-top-design` + `wondelai-refactoring-ui` (taste calibration) |
| High-stakes art-direction decision (new section composition, Nano Banana art-direction, audience pivot) | `think-tank` BEFORE deciding |
| New section composition or brand-asset application | `brand-guidelines` |
| Image / photo generation prompting (Nano Banana, fal, sora) | `generate-image` + `fal-ai-media` |
| Video / motion-graphics composition | `remotion-video-creation` or `manim-video` |
| Mobile responsive sweep | `mobile-design` + `accessibility-auditor` |
| Before final submission / deploy | `web-performance-optimization` + `accessibility-auditor` + `web-quality-audit` |
| PDF export (#9 in queue) | `pdf-processing-pro` |
| Headless screenshot / visual verification | `screenshot` + `screenshot-feature-extractor` |
| Bilingual layout / RTL edge cases | `i18n-localization` |
| Design-token / system poster work | `ui-design-system` + `design-system` |

### Agents — auto-spawn on these triggers

| If the situation is... | Auto-spawn agent |
|---|---|
| Compositional design problem (pillar layouts, grid recipes, typography scales) | `Plan` agent — tight-scope <200 word prompt (§13b Rule 19) |
| After any change touching >150 lines | `code-reviewer` agent on the diff |
| Fresh session, need codebase map | `code-explorer` agent |
| CLAUDE.md / PHASES.md / DNA.md need a real rewrite (not patches) | `tech-writer` agent |
| Multi-section parallel work (3+ independent surgical fixes) | Spawn multiple `general-purpose` or `developer` agents IN PARALLEL via single message |
| Spec-level breakdown of a feature into steps | `tech-lead` agent |
| Award-submission verification pass before declaring DONE | `qa-engineer` agent for LLM-as-Judge rubric |
| Past-mistake check before re-trying something that failed before | `historical-context-reviewer` agent on `index.html` git history |

### Auto-track work with TaskCreate / TaskUpdate

- Any directive with 3+ steps → `TaskCreate` each step upfront, `in_progress` before starting, `completed` immediately after each lands.
- Skip task tracking for single trivial edits or pure Q&A.

### Announce, don't ask

When auto-invoking, state it briefly: "Using `wondelai-web-typography` for the type scale pass" — then proceed. Never ask "should I invoke X?" — the user has pre-authorized everything in this table.

## 4. ASSETS
**Logo (never modify):** `assets/logo-wordmark.svg` · `assets/logo-with-tagline.svg` · `assets/logo-with-rays.svg`

**Primary brand element vocabulary** (Raya's original drawings — use these): `assets/element-stairs-green-new.svg`, `assets/element-arrows-pink-new.svg`, `assets/element-bolt-yellow-new.svg`, `assets/element-semicircle-blue.svg`, `assets/element-spark-orange.svg`. Reserve: `element-banner-ribbons.svg`, `element-squiggle-yellow.svg`. Always rendered via `<img>`, never traced. See §3b for color-to-element pairings.

**Photographic media** (Nano Banana 2 generated, business-grade editorial — Phase 18 / Session 4): `assets/media/s13-01.webp` (open brochure + tea) · `s13-02.webp` (notebook + yellow pencil) · `s13-03.webp` (blank business card) · `s13-04.webp` (letterhead + fountain pen) · `s13-05.webp` (letter alt). Used as CSS `background-image` on `.ap-scene` elements with logo SVG composited as absolute-positioned overlay on the blank paper. Discipline locked: no people, no faces, business-grade still-life only, no cultural-tourism dressing (per the Session-4 panel debate). Future media additions go in `assets/media/` with sequential naming.

**Banned:** `element-rays-burst.svg`, `element-arc-purple.svg`, `element-triangle-orange.svg`, `element-spark-blue.svg`. `element-x-orange.svg` only inside the Misuse section.

**Deprecated** (do not use — the sterile redraws): `assets/system/sys-*.svg` (entire folder). The originals in `assets/element-*.svg` replace them.

## 5. ELEMENT RULES
- Every element drawn on 24u (192px) artboard. Stroke: 6u primary / 3u secondary. Corner radius ≤ 1.5u.
- ≤1 brand colour per element (BURST exception: all 5, one per ray).
- Elements must animate — DRAW or RISE. Never static decoration.

---

## 6. COLOR SYSTEM

Define once in `:root`. Never hard-code hex anywhere else.

```css
:root {
  --c-ink:       #0D0D0D;
  --c-pink:      #FF69B4;
  --c-blue:      #4FC3F7;
  --c-yellow:    #F5D03A;
  --c-orange:    #E07840;
  --c-green:     #8BC48A;
  --c-bg:        #FAF8F3;
  --c-bg-dark:   #0F0F10;
  --c-text-soft: rgba(13,13,13,0.65);
  --c-line:      rgba(13,13,13,0.10);
}
```

### Color Stories — binding creative direction

**الحبري `#0D0D0D` — الأساس** · The weight before understanding. Certainty — when a student reaches their answer, they write it here. Logo, headlines, structure.

**الأصفر `#F5D03A` — اللحظة** · The lightbulb. The exact moment the word falls into place. Hot, charged, impossible to ignore. The colour of إدراك itself. Aha moments, spark element.

**السماوي `#4FC3F7` — الوضوح** · After understanding — clarity. Directly tied to neurofeedback: training the mind toward calm focus. Parent voice, information, cognitive content.

**البرتقالي `#E07840` — الاندفاع** · The moment before breakthrough. Inner fire that refuses to surrender. Energy accent, motion elements, the path before the result.

**الوردي `#FF69B4` — الطاقة** · The student's voice. Courage to try again after failure. Small celebrations. All student-facing communication, social posts.

**الأخضر `#8BC48A` — النمو** · Patience that bears fruit. Slow and certain, like self-confidence. Step motif, progress content, treatment journey.

### Colour-per-section law
One dominant + neutral (`--c-bg` or `--c-ink`) + max one accent. Never all colours equally on one section.

| Section | Dominant | Reason |
|---|---|---|
| Hero | `--c-ink` + rays | weight + burst |
| Brand Story | `--c-yellow` | the إدراك moment |
| Two Voices | `--c-pink` + `--c-ink` | student + parent |
| Colour section | full takeover per colour | immersive demo |
| Neurofeedback | `--c-blue` | focus + clarity |
| Growth content | `--c-green` | patience + stability |

---

## 7. TYPOGRAPHY
- **Arabic:** Cairo 300/400/500/600/700/900 · **Latin:** Lato 300/400/700 · Google Fonts preloaded.
- **Forbidden:** Tajawal · Reem Kufi · IBM Plex Sans Arabic.
- Arabic: lh ≥ 1.8, letter-spacing 0, Western numerals, no tashkeel.

| Role | Size | Weight |
|---|---|---|
| Display | 160–240px | Cairo 900, lh 0.85 |
| H1 | 72px | Cairo 700 |
| H2 | 40px | Cairo 600 |
| Body | 18px | Cairo 400, lh 1.9 |
| Eyebrow | 11px Lato | 400, uppercase, ls 4px |

## 8. LAYOUT — WEB-FIRST
- `<html dir="rtl" lang="ar">`. Logical CSS: `padding-inline-start`, `margin-inline-end`.
- Sections: `min-height: 100vh`, full-bleed. **No A4 dimensions. No `@page`. No `overflow:hidden`.**
- No shadows. No blur. No gradients. No glassmorphism. Baseline grid: 8px.

## 9. MOTION — CINEMATIC GSAP
GSAP + ScrollTrigger via CDN. Required on every section. All gated to `body.live` class.
- **REVEAL** — `clip-path: inset(100% 0 0 0)` → `inset(0)`, 0.6s
- **RISE** — `translateY(40px) + opacity 0` → `0 / 1`, 0.5s
- **DRAW** — `stroke-dashoffset` → 0, 0.8–1.2s (SVG only)
- **SCRUB** — pin + ScrollTrigger scrub for narrative text reveals
- **PARALLAX** — background elements 0.3–0.6× scroll speed

Easing: `cubic-bezier(0.16, 1, 0.3, 1)`. Hover: 4px lift, 0.2s — never scale, never rotate.

---

## 10. BRAND COPY — LOCKED (Raya's words, never edit)

**الرسالة:** نأخذ كل طالب إلى لحظة إدراكه — مهما كانت نقطة بدايته، ومهما كان الطريق.

**الرؤية:** أن يصبح كل طالب يواجه صعوبة في التعلّم قادراً على معرفة كيف يفكّر، كيف يتعلّم، وكيف يُقيّم نفسه — قبل أن يحتاج لأحد يُقيّمه.

**قصة إدراك:** اثنتا عشرة سنة في الميدان علّمتنا شيئاً واحداً: الطالب الذي يُقال عنه "ما بيفهم" — لم يفشل في التعلّم. فشل النظام في أن يجد بابه. إدراك وُلد من هذا الإيمان. نحن لا نُدرّس مناهج. نبني خططاً. خطة لكل طالب بمفرده — تبدأ بتشخيص حقيقي لطريقة تفكيره، وتنتهي بطالب يعرف نقاط قوّته قبل أن يعرف إجابات الأسئلة. أدواتنا تختلف: استراتيجيات تعليمية، تعلّم من خلال اللعب، وجلسات neurofeedback. لكن الهدف واحد: أن يخرج الطالب واثقاً — لا لأنه نجح في الامتحان، بل لأنه فهم كيف يُفكّر. لا نعيد سرد الدروس.. بل نصنع لحظة إدراك.

**لمن نعمل:** للوالد الذي جرّب كل شيء ولم يرَ فرقاً. للطالب الذي أقنع نفسه أنه "مش ذكي".

---

## 11. BUILD RULES
- One section per prompt. Screenshot → verify → gate → next.
- Cost: Sonnet default. Never fabricate to fill space.

**Screenshot (full doc):**
```powershell
& "C:\Program Files\Google\Chrome\Application\chrome.exe" --headless --disable-gpu --hide-scrollbars --virtual-time-budget=8000 --screenshot="C:\PROJECTS\Idrak-Brand-System\qa\all-pages.png" --window-size=1440,5000 "file:///C:/PROJECTS/Idrak-Brand-System/index.html"
```

## 12. WEB SECTIONS

All 15 sections built. Polish phase active.

| # | Section | Status | Composition |
|---|---|---|---|
| 01 | Hero | ✅ DONE | cream + 5 layered brand-`element-*.svg` (dome/stairs/bolt/arrows/spark) + logo SVG protagonist on RTL leading edge + RTL spine + folio + bottom rule |
| 02 | Brand Story | ✅ DONE (rebuilt) | dropped 500vh scrub; now 100vh two-column REVEAL. LEFT: `element-bolt-yellow-new.svg` (yellow's primary element per §3b) + "اللحظة · The moment" caption. RIGHT: eyebrow + mission headline (Cairo 900 with yellow rule) + 3 flowing beats from §10 + final beat "لا نعيد سرد الدروس.. بل نصنع لحظة إدراك" Consistent chrome + foot rule. No ghost numeral — that pattern was removed for cross-section consistency. |
| 03 | Brand DNA | ✅ DONE (3 acts + per-pillar differentiation + poster scale — Sessions 5 & 7) | **Act 1 — `.dna-vision` cinematic scene** (100vh pinned, ScrollTrigger pin+scrub 0.7, 140% scroll length). Five vertical brand-colour bars grow from floor (staggered edges-in), five elements appear with Arabic labels (اللحظة · الاندفاع · الطاقة · الوضوح · النمو), converge to centre as logo SVG fades in as unified mark + "خمس قيم — هوية واحدة." Awwwards screen-record beat. **Act 2 — 5 DIFFERENTIATED pillar scenes** (Session 7 upgrade): the "one move repeated 5 times" knock is resolved. Each pillar carries its story through LAYOUT, not just colour. **1. اللحظة (bolt)** — single-column centered, "strike from sky," vertical yellow line dropping through text spine. **2. الاندفاع (spark)** — asymmetric diagonal thrust, name + desc upper-RIGHT (RTL leading), spark lower-LEFT, orange hairline diagonal connector. **3. الطاقة (arrows)** — arrows row top, name centered below, pink rhythm-dash baseline. **4. الوضوح (dome)** — perfectly centered symmetric, dome over name, blue thin ring framing whole stack as halo. **5. النمو (stairs)** — asymmetric, stairs anchored physical-LEFT bottom, name + desc physical-RIGHT, green 5-tick ladder on physical-LEFT margin (= the 5 steps of growth). Per-pillar `.dna-pillar--X` CSS overrides drive everything from same HTML — no markup change. **Act 3 — `.dna-system-overview` Vignelli-grade system poster** (Session 7 upgrade from Phase 19): five horizontal bands (COLOUR / ELEMENT / ICON / TYPE / MOTION). Massive ghost numeral (`clamp(72px, 8vw, 120px)` Lato 300 @ 14% opacity), 88px Cairo 800 Arabic name, tracked Latin caption — each band declares a system primitive with manifesto weight. Plan-agent-derived typography (number 120 / Arabic 88 / Latin 13 / label-col 280px / band-padding 36px). Counter stays `03 / 15`. `?act=N` URL flag (1/2/3) for isolated headless capture |
| 04 | Two Voices | ✅ DONE | split-column with center hairline — student (pink/arrows) on physical left, parent (blue/dome) on physical right, elements anchored opposite their text, differentiated parallax per column |
| 05 | Colour System | ✅ DONE | 6 full-bleed scenes (ink + 5 brand colors). Orange scene applies `filter: brightness(0) invert(1)` on the element so the orange spark reads against the orange field (white watermark). Other scenes use the element's native colour |
| 06 | Typography | ✅ DONE (Session 6 — letterform spread REMOVED) | bilingual specimen spread (Act 1) — Lato column left / Cairo column right divided by hairline, 5 specimen rows. Display specimen capped at `clamp(56px, 6vw, 96px)`. **Phase 19 letterform sub-spread DELETED in Session 6**: claimed "Cairo's إدراك generates the green stair heights" — factually wrong (Cairo is typography, NOT the logo font; the actual logo letterforms live in `logo-wordmark.svg`, not Cairo). Plus it set 5 typeset إ-د-ر-ا-ك letters at `clamp(96px, 13vw, 180px)` = §3 + §13b Rule 2 violation. **NEW LOCKED RULE: Cairo is the brand's TYPOGRAPHY font (body, headlines, content). It is NOT the source of the logo letterforms. Never claim Cairo "generates" the system — the logo SVG is its own custom drawing.** Specimen spread stands alone now. |
| 07 | Elements | ✅ DONE (Session 6 — icon system rewritten to UI library) | 5-card grid (Act 1, unchanged) — moment / drive / energy / clarity / growth. **Act 2 — Service Icons · UI Library** (Session 6 rebuild). Phase 19's "15 icons derived from element silhouettes" was a designer's puzzle, not a usable icon set. Replaced with **20 icons in 3 functional groups, tied to BUSINESS not brand-shapes**: **SERVICES** (Diagnosis · Personal Plan · Neurofeedback · Play-based · Strategies · Progress · Evaluation · Confidence), **AUDIENCE & CONTACT** (Student · Parents · Phone · Email · Location · Schedule · Teacher · Resources), **UI UTILITY** (Menu · Search · Download · Share · Expand · Close · Settings · Print). Single-stroke 24×24 viewBox, stroke 2u, round caps/joins, bilingual labels per icon (Cairo 600 + Lato 700 tracked). Each group has a header label with brand-colour rule and a group number. Real UI library tuned for the website + future surfaces. Per-icon RISE + per-group stagger via GSAP. **NEW LOCKED RULE: Icons in a brand book serve the BUSINESS (services, audience, UI), not the brand shapes. Element-derived icon families look like a puzzle, not a usable set. Use real UI conventions (Lucide/Phosphor visual grammar) tuned to brand voice.** |
| 08 | Logo Variations | ✅ DONE | 3-card grid — primary wordmark / with tagline / with rays — RISE motion |
| 09 | Logo Anatomy | ✅ DONE | restructured. Centered SQUARE `.anat-frame` holds logo + construction grid + anchor dots in ONE coordinate space. Labels positioned OUTSIDE the frame at `calc(100% + 40px)` with leader hairlines — never clip at section edges. Diagonal callout lines removed (they were mis-aligning across non-square stage) |
| 10 | Clear Space | ✅ DONE | REVEAL diagram + 1x/2x/x legend |
| 11 | Logo on Backgrounds | ✅ DONE | 7 surfaces + rule card, hairline grid |
| 12 | Logo Misuse | ✅ DONE | 6-card grid + REVEAL X-mark stamps |
| 13 | Applications → **Stationery System** | ✅ DONE (rebuilt — Session 6, all 3 logo variants now used) | Photographic encounters from Session 4 were "empty papers with logo pasted" — meaningless mockups. **Session 6 rebuild**: 4 designed flat-style stationery artifacts using all 3 logo variants with discipline. **01 Letterhead (A4 landscape, 16:9)** — `logo-with-tagline.svg` top-left, Arabic body type (recipient + 2 body paras + yellow-rule accent quote "لا نعيد سرد الدروس.. بل نصنع لحظة إدراك" + signature). **02 Business Card · Front (85:55)** — `logo-wordmark.svg` top, name (راية عبد الحي) + role + contact bottom-right, yellow rule on RTL leading edge. **03 Business Card · Back** — yellow takeover, `element-bolt-yellow-new.svg` (ink filter) + tagline "نصنع لحظة إدراك" + English subtitle. **04 Social Post (1:1)** — `logo-with-rays.svg` centered, celebratory message + pink hashtag. Layout: hero letterhead full-width, then 3-column row. NEW LOCKED RULE: every brand book MUST USE every logo variant somewhere — variants without application = wasted assets. Photo-composite path from §13b Rule 14 preserved for future Nano Banana media. |
| 14 | Motion Demo | ✅ DONE | 4 live CSS loop primitives (REVEAL / RISE / DRAW / LOOP) |
| 15 | Closing | ✅ DONE (stillness upgrade — Session 4) | Yellow takeover. Mic-drop quote split into **8 word-spans** (`.cl-w`) revealing one-at-a-time (0.55s stagger + blur-removal, ~5s total) — then a deliberate **4-second silence** before English subtitle, signature, and contact band emerge. Villeneuve's patient counter to S03's maximalism. Follows §13b Rule 11: words default-visible in HTML, GSAP `from()` adds entry as decoration only. English subtitle now has `dir="ltr"` (§13b Rule 12) — the trailing period bidi-bug is fixed. The Brand-actor cursor hides over `.cl-quote` so the type carries this beat uninterrupted |

## 13. RECURRING PATTERNS — implementation discipline

- **RTL text anchor.** Text on the RTL leading edge (physical right): `margin-inline-end: auto` + `text-align: start` (in RTL, start = right). NOT `margin-inline-start: auto` — that pushes the box LEFT in RTL and the wide Arabic words overflow leftward off-canvas. Element on the RTL trailing edge (physical left): absolute positioning with physical `left` / `top`.
- **Bidi-isolated Arabic in bilingual boxes.** Big Arabic display words inside grid/flex containers need `unicode-bidi: isolate` + explicit `text-align: right` — without isolate, bidi reordering breaks alignment.
- **Numeric counters need `dir="ltr"` in RTL context.** `<span dir="ltr">13 / 15</span>` — without this, the section context flips the numeric tokens visually so "13 / 15" renders as "15 / 13". Apply on every section counter, every "X / Y" pattern.
- **Specimen grid hairlines.** `grid-template-columns: repeat(N, 1fr); grid-column-gap: 1px; background: var(--c-line);` with card children setting `background: var(--c-bg)` — produces clean 1px ink hairlines between cards without extra divider elements.
- **Element bleed restraint.** Brand `element-*.svg` shapes have ~50% transparent padding in their viewBox. Sizing containers ~1.7× the visible-shape target works. Don't bleed elements more than ~10% past container edges or they read as slivers.
- **Same-color element on same-color background.** When a brand element sits on its own colored field (orange spark on orange bg, pink arrows on pink bg, etc.), the element disappears. Apply `filter: brightness(0) invert(1)` to render it white, or `filter: brightness(0)` to render it ink. Pair with reduced opacity (`0.7` on dark bg, `0.22–0.25` on light bg) so it reads as a confident watermark, not a competing star.
- **SVG coordinate alignment in non-square stages.** If a diagram has multiple SVG layers (grid + callouts + dots) and a positioned subject (the logo), wrap everything in a SQUARE container (`aspect-ratio: 1 / 1`) so all child `viewBox="0 0 100 100"` references share the same coordinate system. NEVER use `preserveAspectRatio="none"` on layers that need to align with positioned subjects — they stretch differently and coordinates drift.
- **Display type sizing inside narrow columns.** `clamp(min, vw-based, max)` uses VIEWPORT width, not column width. In a 2-column spread, viewport-based display sizing overflows the column. Cap aggressively (e.g. `clamp(56px, 6vw, 96px)` for display in a half-viewport column) and add `overflow-wrap: break-word` as safety.
- **Screenshot mode bypass.** `?screenshot=true` URL param skips all GSAP and sets static "final state" inline styles. Required because Chrome headless doesn't complete RAF timelines reliably. Every section's animations must have a corresponding screenshot-mode static state.
- **Programmatic scroll for headless screenshots.** `?scrollTo=N` URL param scrolls window to pixel N after load. Use with `--window-size=1440,900` to capture a specific section (e.g. `?screenshot=true&scrollTo=1800` for the third section). Note: Chrome's `--virtual-time-budget` may not always let the deferred scroll fire — for reliable verification use the live preview panel instead.
- **Chrome consistency across sections.** Every section uses the same chrome pattern: `<header>` with two spans — left: `<b>NN · English Title</b><span class="*-chrome-title-ar">العربية</span>`; right: `<span dir="ltr">NN / 15</span>`. Section number always ink bold, Arabic in Cairo medium 13px, counter always LTR. No section-specific ghost numerals, no decorative variations — chrome is system furniture, not section art. Implementation: one global override CSS block at the END of `<style>` that targets every per-section chrome class with a canonical typography + spacing rule. Don't refactor each section's HTML — override their CSS variants in one place.

## 13b. OPTIMIZATION RULES — lessons learned (LOCKED)

These are mistakes that were paid for. Don't repeat them.

### 1. Surgical-scope law
When the user says "fix X", touch ONLY X. If you see Y nearby that looks like it needs the same treatment, **ASK first** — don't auto-apply. Two weeks of revisions came from over-reaching small requests into multi-section rewrites. The phrase "while I'm in there" is banned.

### 2. The إدراك audit (run before claiming any section DONE)
Grep for `>إدراك<` (the brand word as raw text outside an `<img alt>`). Every match in a display context (Cairo + weight 700+ OR `clamp(*px, *vw, *px)` for font-size) is a §3 rule violation. The S14 REVEAL primitive used typeset `إدراك` for weeks before it was caught. The ONE exception is the Misuse section card #6 (`.ms-w-recreate`) which intentionally demonstrates the violation.

### 3. RTL physical-axis cheat sheet (LOCKED — memorise)
| Logical property | LTR maps to | RTL maps to |
|---|---|---|
| `inset-inline-start` | physical LEFT | physical RIGHT (RTL leading) |
| `inset-inline-end` | physical RIGHT | physical LEFT (RTL trailing) |
| `padding-inline-start` | padding LEFT | padding RIGHT |
| `padding-inline-end` | padding RIGHT | padding LEFT |
| `margin-inline-start: auto` | pushes box RIGHT | pushes box LEFT |
| `margin-inline-end: auto` | pushes box LEFT | pushes box RIGHT |
| `border-inline-start` | border LEFT | border RIGHT |
| `text-align: start` | aligns LEFT | aligns RIGHT |
| `text-align: end` | aligns RIGHT | aligns LEFT |
| `flex-direction: row` + `justify-content: flex-start` | first item on LEFT | first item on RIGHT |
| `grid-template-columns: A B` | A on LEFT, B on RIGHT | A on RIGHT, B on LEFT |

**The recurring trap:** `inset-inline-end` SOUNDS like "the end of the box" (physical right). In RTL it's physical LEFT. When unsure, just use physical properties (`left`, `right`) for one-shot positioning.

### 4. Same-color-on-color elements
Banned: rendering a brand element with `filter: brightness(0) invert(1)` as a SOLID FLAT FILL on its own colored field — reads as a sticker. Acceptable treatments when forced into this case:
- **Thin architectural outline** — recreate the shape with `border` + `border-radius` (see S13 IG story dome: 2px cream outline + ink-dot apex).
- **Low-opacity ink watermark** — `filter: brightness(0); opacity: 0.22-0.32` (see S13 letterhead orange spark).
- **Scrap the element** — let the brand color carry the canvas alone (see Colour System: most scenes use cream background so element shows natively).

### 5. Bento aspect-ratio law
If `grid-template-columns: A B C` has DIFFERENT fr values AND children have `aspect-ratio`, the wider columns produce TALLER children (aspect-ratio scales height with width). Result: row heights diverge and content overflows / sections balloon. **Fix one of three ways:** equalize columns (`repeat(N, 1fr)`), use realistic-per-spec aspects (a business card = `55/85`, an A4 letter = `210/297`), OR drop aspect-ratio and use `max-height` / fixed heights.

### 6. Screenshot-mode is a separate render contract
Every new motion/animation/curtain/observer-driven effect MUST have a `?screenshot=true` bypass that pre-resolves to final state. Test headless before claiming done. The intro curtain blanked every headless capture until the screenshot-mode bypass was added — caught only after deploy.

### 7. The "would I screenshot this?" test
Before claiming a section DONE, look at it and ask: would I send a screenshot of this to a designer friend? If the honest answer is "competent, but no" — it's a template. Rebuild. This is the difference between "passes review" and "shipped".

### 8. First-visit cinematic gates
Any cinematic > 1.5s deserves a `sessionStorage` gate so it plays once and not on every page reload. Big intros are precious. Firing them on every visit kills the magic and frustrates users navigating between sections. Always pair with a skip control and `prefers-reduced-motion` guard.

### 9. No animation without meaning
Every animation in this book must answer: *does this make the closed door more clearly open?* (the brand thesis, §3c). If the answer is "no, but it's pretty" — banned. Decorative animations make a brand look insecure.

### 10. Pre-flight checklist before claiming DONE
- [ ] `grep ">إدراك<"` — no typeset display matches outside the Misuse demo card
- [ ] Headless capture (`?screenshot=true&audit=true&only=sNN`) — section renders fully, no clipping, no blank cards
- [ ] **Verify in LIVE mode too** — `?screenshot=true` bypasses GSAP and IntersectionObservers, so it can mask runtime bugs. Hard-reload (Ctrl+Shift+R) and scroll into the section before claiming done
- [ ] Visual RTL check — Arabic anchors physical RIGHT, English / numerics anchor physical LEFT
- [ ] Chrome inspection — every counter `dir="ltr"`, every Arabic chip Cairo 13px medium ink
- [ ] Reduced-motion check — `@media (prefers-reduced-motion: reduce)` paths defined for any new animation
- [ ] Element-on-color audit — no flat-fill brand element on its own color field

### 11. Default-visible, opt-IN to animation — never opt OUT of invisibility
**Banned pattern:** CSS that hides critical content by default and depends on JS to reveal it.
```css
/* DANGEROUS — content hidden by default, JS must run perfectly to show it */
.reveal-rtl { clip-path: inset(0 0 0 100%); }
.reveal-rtl.is-revealed { clip-path: inset(0); }
```
If the observer's threshold isn't met, GSAP errors before reaching the observer setup, the element renders taller than expected, or any one of a dozen runtime conditions fails — **the content stays invisible forever**. The S02 Arabic mission line was held hostage by exactly this pattern.

**Required pattern:** content visible by default. GSAP `from()` or equivalent ADDS motion as a layer; if motion fails, content still renders.
```css
.st-headline { /* no clip-path, no opacity tricks. Visible by default. */ }
```
```js
gsap.from('.st-headline', { opacity: 0, y: 24, scrollTrigger: trigger });
// from() sets the "before" state; failure to play = final state = visible.
```
Rule: every load-bearing piece of text MUST render readably with zero JavaScript. Animation is decoration over a working static page, never a gate to seeing it.

### 12. Latin paragraphs in RTL containers need `dir="ltr"`
Already locked for numeric counters (§13). Extension: **any English/Latin paragraph with embedded Arabic words** (e.g. "We take every student to their moment of إدراك …") needs `dir="ltr"` on the wrapper, or bidi will reorder tokens — periods jump to the start of lines, the inline Arabic word splits the sentence visually, etc. The S02 English subtitle had this exact bug.

| Container | Fix |
|---|---|
| `<span>13 / 15</span>` (counter) | `<span dir="ltr">13 / 15</span>` |
| `<p>We take ... إدراك ... path.</p>` (Latin para in RTL section) | `<p dir="ltr">` |
| `<code>npm run dev</code>` inline | wrap in `<span dir="ltr">` |

### 13. Universal section effects need an exemption list, not an apology
Any "every section gets X" pattern (the `section[id]::after` punctum, a universal scroll cue, a corner badge) WILL collide with sections whose content already lives at that position. The motion-v2 punctum at `top: 36px; inset-inline-start: 36px` (RTL physical right) collided with S02's right-column eyebrow. Fix wasn't to remove the punctum — it was to maintain `.s-XXX::after { display: none; }` for every section where the position is occupied. Audit ALL sections when adding any universal effect:

Current punctum exemptions: `.s-hero` · `.s-brand-story` · `.colour-scene` · `.s-closing`. Add new ones the moment you spot a collision.

### 14. Photo-composite pattern for applications (LOCKED — Session 4)
When mocking up branded artifacts (cards, letterheads, brochures) **never typeset the brand mark into the photo via AI prompts**. Nano Banana 2 will distort `إدراك` letterforms — Brand New jurors will spot it instantly. Required pattern:

1. **Generate the photo with BLANK paper** — prompt explicitly says "no text, no logos, blank cream paper for compositing."
2. **Use the photo as a CSS `background-image`** on the `.ap-scene` element, NOT as an `<img>` tag. This way a missing-file fallback is just the cream `background-color` showing — no broken-image icon ever.
3. **Composite the actual `assets/logo-wordmark.svg`** as an absolute-positioned child `<img>` via CSS `.ap-scene-logo--{slot}` classes. Position per-photo with `top` / `inset-inline-start` / `inset-inline-end` / `width` / `transform: rotate()`.
4. **Logo stays pixel-perfect** (real SVG, not raster), swappable (change `logo-wordmark.svg` → `logo-with-tagline.svg` and every photo updates), and on-brand in any Arabic/Latin direction.
5. **For Arabic-reading-direction surfaces** (brochure spreads, letters, anything with a "front" page): logo goes on the **right page** = `inset-inline-start` in RTL. The brochure logo in S13 was wrong on first composite (it was on the left page); the fix was flipping `inset-inline-end: 24%` → `inset-inline-start: 26%`. Always test which page the AI rendered as the "open spread leading edge" and put the logo there.

### 15. Generated media discipline (LOCKED — Session 4)
- **Format:** Nano Banana 2 outputs `image/webp` natively. Don't fight it — keep `.webp` in `assets/media/` and reference `.webp` in HTML. WebP is smaller than JPG and universally supported in modern browsers.
- **People:** banned. The brand panel debated this — people-in-photos add one more category of AI failure (faces, hands, expressions). Still-life only. Notebook + pencil > student at desk.
- **Cultural-tourism dressing:** BANNED across all series (photo, illustration, video, social). The brand language is Arabic because the audience reads Arabic, not because the brand is "Arab-themed." Banned visual cues: hijab, thobe, traditional dress, calligraphy on walls, Arabic-mosaic patterns, religious framing, geographic markers (Tira/Palestine/Levantine props), "Arabic coffee" scenes, kitchen-warmth tropes. Generic premium global editorial — like Apple's education ads, where Arabic appears as language not as setting. **The brand serves any kid struggling with learning, anywhere — universal-young-person register.** The user has locked this twice now (Session 4 + Session 8). DO NOT ask "should we add hijab/cultural elements?" in any future session — the answer is permanently no.
- **Six-eight photo budget per section.** Erik's discipline level. Each photo must be prompt-engineered like a production still (specific lighting, lens, color palette in the prompt). No "moody background AI" wallpaper.

### 16. Section as multi-act narrative (Session 4 pattern, opt-in)
A section that's both an Awwwards-cinema beat AND a Brand-New-system spread can be structured as **Act 1 (cinematic vision) + Act 2 (educational breakdown)** stacked inside the same `<section id="sNN">`. S03 is the reference implementation: `.dna-vision` (100vh pinned ScrollTrigger scrub) followed by 5 `.dna-pillar` scenes. The chrome counter stays "03 / 15" across both acts — it's still one section. Apply this pattern when a section needs to do two jobs at once. Don't apply it everywhere — most sections should remain single-act.

### 17. Per-pillar compositional differentiation (Session 7 — LOCKED)
**Banned pattern:** when a section has 5+ "pillar scenes" that share content slots (eyebrow + name + desc + element + counter), do NOT repeat the same `grid-template-columns: 1fr 1fr; text-right; element-left` layout 5 times. A judge flipping through the book will conclude "they have one move." This is the most common award-submission downgrade.

**Required pattern:** every pillar scene varies at LEAST 3 of these 6 axes:
1. Grid (single-column vs split vs 12-col vs band)
2. Element placement (center vs corner vs full-bleed vs anchored)
3. Text alignment (centered vs RTL-leading vs asymmetric)
4. Accent treatment (vertical bar vs ring vs diagonal vs tick-ladder vs dashed-rhythm)
5. Vertical rhythm (centered vs top-anchored vs bottom-anchored)
6. Composition mood (symmetric calm vs asymmetric thrust vs marching band)

Reference implementation: S03 Act 2's 5 pillars — each gets a unique `.dna-pillar--X` CSS override block driving its own composition. Same HTML, different CSS. Use `Plan` agent with tight scope (<200 words) to design the 5 gestures BEFORE coding.

### 18. Cairo is typography, NOT the logo font (Session 6 — LOCKED)
Cairo is the brand's **typography** font (body, headlines, content). The brand mark `إدراك` in `assets/logo-wordmark.svg` has its **own custom letterforms** — they are NOT Cairo glyphs.

**Banned claim:** "Cairo's إدراك generates the system" — factually wrong. The logo letterforms are unique drawings; Cairo letterforms are different shapes that happen to spell the same word.

**If you want to show "type generates the system":** measure the actual `logo-wordmark.svg` paths (extract heights from the real SVG), not Cairo's إدراك at 180px display scale. Setting Cairo's إ-د-ر-ا-ك at display weight ALSO violates §3 (logo recreation in CSS) — double violation.

Cairo and Lato are the brand's typographic SYSTEM. The logo is the brand's MARK. Different categories. Don't conflate.

### 19. Plan-agent tight-scope pattern (Session 7 — workflow)
When context is bloated (>300 tool calls / strategic-compact reminder firing), `Explore` agents will fully refuse, but `Plan` agents still work IF the prompt is **under 200 words with concrete output requirements**. Pattern that landed twice this session:

1. State the design problem in 2-3 sentences (what's being designed, what constraints)
2. List the existing state (numbers / specific selectors / what currently fails)
3. Give the precise output shape ("for each X, give me: 1-line headline + grid recipe + accent treatment") with a word cap
4. End with explicit constraint reminders (locked rules from CLAUDE.md)

Returns: actionable CSS numbers / compositional recipes that translate directly to code. Used for: S03 pillar differentiation (5 gestures), S03 system poster typography (6 sizes). Both shipped same-session.

### 20. Mobile sweep — single @media block + actual class names (Session 8 — LOCKED)
Mobile-responsive pass for this codebase = ONE new `@media (max-width: 600px)` block at the END of `<style>` (post-line 4874). Source-order beats the existing 900px tablet rules without specificity hacks.

**The non-negotiable rules learned in Session 8 (paid in re-screenshot iterations):**
1. **Always grep for actual class names before writing selectors.** `.elements-grid` (not `.el-grid`), `.element-card` (not `.el-card`), `.logo-var-grid` (not `.lv-grid`), `.voices-split` + `.voice-col` (not `.tv-*`), `.mo-grid` + `.mo-card` (not `.mt-*`), `.anat-label` (not `.anat-callout`), `.art-lh-head/body/para` (not `.art-letterhead-body`), `.ap-headline-ar` (not `.ap-hero-ar`). Guessing class names = 2 wasted rounds of screenshots.
2. **Chrome stacks 2-line on phone, doesn't truncate.** The unified rule at ~line 4770 sets `.X-chrome > span:first-child { display: inline-flex; }` which blocks `flex:1 + min-width:0` ellipsis. Fight it via `flex-wrap: wrap` + put counter span `order: -1` + `flex-basis: 100%`. Cleaner than truncation.
3. **`html, body { overflow-x: hidden; max-width: 100vw }` is mandatory.** Otherwise any internal overflow creates a horizontal scrollbar on phone and the visible viewport reads as wider than 375.
4. **Construction labels positioned `right: calc(100% + 40px)` cannot exist on phone.** Hide them on `< 600px` — the diagram alone still communicates intent. S09 anatomy is the reference case.
5. **Latin paragraphs in RTL sections must have `dir="ltr"` in HTML** to avoid bidi reordering at narrow widths. The text wraps fine at desktop because line-breaks hide the reorder; at 375 the reorder is visible. This is an HTML edit, NOT a CSS-only fix — schedule a separate sweep.
6. **Verification cadence:** capture per-section at 375 (`?screenshot=true&only=sNN`, `--window-size=375,900`), not full-doc 14000px tall — detail compresses too far in the stacked view to spot real breaks.

Reference implementation: `index.html` lines ~4877–5170 (the `@media (max-width: 600px)` block).

## 13c. HEADLESS SCREENSHOT TOOLKIT — working approach

The verified, reproducible setup. Don't fight Chrome — use the URL flags built into the page.

### URL flags (cumulative)
| Flag | Effect |
|---|---|
| `?screenshot=true` | Bypass GSAP, pre-resolve clip-paths, mark all sections `has-entered`, remove intro curtain + skip button |
| `?audit=true` | Lock every section to exactly 900px tall (override `min-height: 100vh`) so the whole doc stacks at predictable y-offsets |
| `?only=s13` or `?only=s02,s13` | Hide every section EXCEPT the listed ids — capture one section in isolation |

### Reliable capture commands

**Single section (above-fold):**
```powershell
& "C:\Program Files\Google\Chrome\Application\chrome.exe" --headless --disable-gpu --hide-scrollbars --virtual-time-budget=10000 --screenshot="C:\Projects\Idrak-Brand-System\qa\sNN.png" --window-size=1440,900 "file:///C:/Projects/Idrak-Brand-System/index.html?screenshot=true&only=sNN"
```

**Single section (full content, taller capture):**
```powershell
--window-size=1440,1800   "file:///C:/.../index.html?screenshot=true&only=sNN"
```

**Multi-section audit stack:**
```powershell
--window-size=1440,2800   "file:///C:/.../index.html?screenshot=true&audit=true"
```

### Known limits & quirks
- **Chrome max screenshot height ≈ 16384px** (2^14). Captures taller fail silently with no file written.
- **`vh` units stretch with render-window height** — if you don't use `?audit=true`, a 1440×15000 capture makes 100vh = 15000px and only section 01 fits the frame.
- **`?scrollTo=N` is unreliable in headless** — `--virtual-time-budget` doesn't always let the deferred scroll fire. Use `?only=sNN` instead.
- **PowerShell stderr from native exes** registers as `RemoteException` even on success. Pipe `2>&1 | Out-Null` and verify file existence separately, not exit code.
- **Chrome can lock from prior `--headless=new` runs** — kill `chrome.exe` processes before a fresh capture if files stop writing.

### Image extraction from chat (Session 4 trick)
When the user pastes Nano-Banana-generated (or any) images into the Claude Code chat, the bytes can't be moved to disk by the AI's tools directly. BUT the images are stored as base64 in the session transcript at `C:\Users\vanez\.claude\projects\C--Projects-Idrak-Brand-System\<session-uuid>.jponl`. The script at **`qa/extract-images.ps1`** reads the tail (~80 MB) of that JSONL, regex-matches `"type":"image","source":\{"type":"base64","media_type":"([^"]+)","data":"([^"]+)"\}`, and writes the N most-recent images to `assets/media/`. Re-usable for any image-attachment turn — adjust `$wanted` and the output filename pattern. Output extension is derived from `media_type` (Nano Banana 2 outputs `image/webp` so files land as `.webp`). After extracting, verify slot order by `Read`-ing the resulting files — Nano Banana doesn't preserve upload order in the transcript reliably.

## 13d. COPY-REWRITE PHASE — IN PROGRESS

A copywriter is rewriting all visible text. Working file: **`COPY.md`** (root of repo). The file lists every visible string in the book, organized by section, with `🔒 LOCKED` flags on Raya's words (from §10) that must NOT be touched.

### Session 3 — batch 1 landed (May 2026)

**Decision rule applied:** "Keep current English, replace Arabic only where new Arabic differs from old AND fits the existing slot." Long-Arabic replacing short-chip cases (S10 legend, S11 rule card) deferred until a layout pass can accommodate them. S03–S07 Arabic-only descriptions (where new draft removed English entirely) deferred — keeping current English per user instruction.

**14 Arabic deltas applied + founder name correction:**

| Section | Old | New |
|---|---|---|
| S02 punctum tag | `الصاعقة التي يأتي بها الإدراك — البرق الذي يفتح الباب.` | `الومضة التي يولد بها الإدراك — البرق الذي يُشرع الباب.` |
| S08 variation 01 | `الشعار الأساسي` | `الشعار المطلق` |
| S09 anatomy headline | `الشعار مرسوم — ليس مكتوباً` | `الشعار يُرسم — ولا يُطبع` |
| S10 clear-space headline | `يحتاج الشعار إلى مساحة ليتنفّس` | `مساحة الشعار مقدسة` |
| S11 backgrounds headline | `الشعار يحافظ على كامل تباينه على كل خلفية` | `حضور صلب على كل خلفية` |
| S12 misuse headline | `لا تعدّل الشعار — أبداً` | `الشعار كيان مغلق — يُمنع المساس به` |
| S12 misuse rules ×6 | `لا ت…` voice | formal `يُمنع …` voice |
| S13 applications headline | `الهوية حيّة — على المنشور والبطاقة والورقة` | `الهوية في الميدان — تتحدث بوضوح وثبات` |
| S13 letterhead body | `يسعدنا أن نشارككم خطّة طفلكم …` | `نضع بين أيديكم مسار طفلكم …` |
| S13 + S15 founder name | `ريّا عبد الحي` | `راية عبد الحي` |

All 🔒 LOCKED phrases verified untouched. `COPY.md` mirrored. Stale-string sweep clean.

### When the next batch of rewritten copy arrives
1. Diff the copywriter's revised `COPY.md` against the current source-of-truth (which now reflects batch 1 above).
2. For each changed block, find the matching string in `index.html` and replace it surgically — touch nothing else.
3. After the swap, run the pre-flight checklist (§13b #10). Pay special attention to:
   - **Display headlines** — Arabic clamp-sized type can overflow narrow columns if word-count grew >20% (§13 display sizing rule). Bump max-clamp down if needed.
   - **Beat line-spacing** — long Arabic paragraphs need `line-height: ≥ 1.85`. New copy may need lh re-tune.
   - **RTL anchoring** — verify Arabic text still anchors physical right after rewrite.
   - **Latin paragraphs with embedded Arabic** — add `dir="ltr"` (§13b rule 12).
4. Headless screenshot every affected section post-swap **AND** verify in live mode (§13b rule 10).

### LOCKED — Raya's words that can NEVER change
From §10 — these strings appear multiple times and are the brand's spine. Do not touch even if the copywriter suggests alternatives:
- `نأخذ كل طالب إلى لحظة إدراكه.` (S02 headline, S06 H2 spec, S13 hero quote)
- `لا نعيد سرد الدروس.. بل نصنع لحظة إدراك` (S02 final beat, S06 H1 spec, S15 mic-drop)
- `للوالد الذي جرّب كل شيء — ولم يرَ فرقاً.` (S04 parent quote, S13 IG story)
- `الذي أقنع نفسه أنه «مش ذكي».` (S04 student quote)
- The four S02 brand-story beats (Arabic only)

The English equivalents CAN be rewritten — but they must preserve the meaning of these locked Arabic phrases. The copywriter has been briefed on this in `COPY.md`.
