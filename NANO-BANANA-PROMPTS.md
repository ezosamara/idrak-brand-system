# NANO-BANANA-PROMPTS.md — إدراك Brand System

Production-ready prompts for Nano Banana 2 image generation. Three series.
Generated to match the brand's locked discipline (CLAUDE.md §3b, §3c, §13b Rules 14–16).

---

## Discipline preamble — apply to EVERY prompt

**Brand thesis:** إدراك is the moment a closed door opens. Every image must feel like one quiet moment of perception, not a stock-photo busy scene.

**Hard rules:**
- **Palette:** cream `#FAF8F3` field, ink `#0D0D0D` for shadow/weight, plus the 5 brand colors as accents — pink `#FF69B4`, blue `#4FC3F7`, yellow `#F5D03A`, orange `#E07840`, green `#8BC48A`. **One accent dominates per frame; never use all five together.** Never pure white `#FFFFFF`.
- **NO cultural framing.** Premium global-editorial register (Apple education ads, Pentagram annual reports). Arabic is the brand's language because the audience reads Arabic — NOT a theatrical setting. **Banned across every series:** hijab, thobe, calligraphy on walls, Arabic-mosaic patterns, traditional dress, religious framing, geographic markers (Tira/Palestine/Levantine visual cues), Arabic coffee props, "kitchen scene" warmth. Generic premium environment. The viewer should feel quality, not location. The brand serves any kid struggling with learning, anywhere.
- **No typeset Arabic text in the image.** Nano Banana distorts `إدراك` letterforms — brand jurors will spot it instantly. Every photo composites the real `logo-wordmark.svg` via CSS on top of blank paper / blank surface generated in the prompt.
- **Output format:** WebP, 4:5 or 3:2 or 1:1 aspect. Resolution: 2048px long-edge minimum.
- **Light:** Soft directional north-light or low-angle warm window light. No flash. No HDR drama. No lens-flare. Cinematographer references: Roger Deakins quiet, Bradford Young patient. NOT Annie Leibovitz dramatic, NOT Wes Anderson symmetric.
- **Depth of field:** Shallow but believable (f/2.8–f/4 feel). Subject sharp, background softly cushioned. No fake bokeh-blur halos.
- **Avoid:** lens flare, vignettes, instagram filters, magic-hour orange, oversaturated colors, AI-tell symmetry, cluttered backgrounds, motivational-poster typography, "Arabic mosaic" patterns, hijab clichés in D2.

---

## Series D1 — Still-life (no people)

**Purpose:** Stationery + applications imagery for Section 13 expansion + future surfaces. Used as CSS `background-image` on `.ap-scene` containers with `logo-wordmark.svg` composited as a positioned overlay (§13b Rule 14).

**Format:** 5 photos. WebP. 2048×2560 (4:5) for verticals, 2560×1707 (3:2) for horizontals.

### D1-01 — Open notebook + yellow pencil on cream desk · 3:2 horizontal
```
A clean overhead-3/4 shot of a single open A5 notebook on a cream-painted oak desk. The notebook pages are completely blank, off-white textured paper, no lines, no printing — soft natural cream tone. A slim yellow #F5D03A wooden pencil rests diagonally across the right page, eraser end pointing toward the camera. Soft north-window light enters from the upper left, casting a long quiet shadow of the pencil across the page. Color palette: cream desk, off-white paper, single yellow accent (the pencil). Ink-black graphite point catches the light. Background out of focus, just a darker cream wall corner suggesting depth. Editorial still-life, Bradford Young patient lighting, Kinfolk magazine restraint. NO text, NO logos, NO typography, NO additional objects. Shot on Hasselblad H6D-100c, 80mm lens, f/3.5, ISO 100. WebP output 2560×1707.
```

### D1-02 — Single business card on textured cream paper · 1:1 square
```
Tight overhead macro of one matte-cream blank business card (85mm × 55mm) resting at a slight 4-degree rotation on a larger sheet of off-white art paper with very fine grain texture. The card is completely blank — pure cream face, no printing, no embossing. A single soft shadow under the card suggests it sits 1mm above the paper. Light is diffused window-light from camera-right, cool morning temperature. Empty negative space top and bottom. Color palette: monochrome cream with one whisper of warm ink shadow. NO text, NO logos, NO marks, NO secondary objects. Shot on Phase One IQ4, 120mm macro, f/4, ISO 50. WebP output 2048×2048.
```

### D1-03 — Blank A4 letterhead with fountain pen at rest · 4:5 vertical
```
A vertical overhead shot of a single blank A4 sheet of premium cream cotton paper centered on a darker textured tabletop (deep warm ink-black wood with fine grain). The paper is perfectly blank — no header, no text, no watermark, no logo, just clean cream. A matte-black fountain pen lies diagonally across the lower-right corner of the paper, cap on, no markings visible. A small folded cream envelope sits in the upper-left, partly off-frame. Soft cool morning light from the upper-right corner. Color palette: cream paper, deep ink wood, matte-black pen. NO text anywhere in the image, NO logos, NO writing on paper. The mood is "letter not yet written, decision not yet made." Shot on Hasselblad H6D, 80mm, f/4, ISO 100. WebP output 2048×2560.
```

### D1-04 — Closed folded brochure on linen with pink ribbon · 3:2 horizontal
```
Editorial overhead-3/4 of a single tri-fold brochure (210mm × 99mm closed) lying flat on a textured cream linen surface. The brochure is completely blank cream cardstock — no print, no logos, no graphics, just folded matte paper. A slim pink #FF69B4 silk ribbon lies in a gentle S-curve across the linen to the right of the brochure, like a bookmark dropped in passing. Soft window light from upper-left, long quiet shadow from the brochure. Color palette: cream + linen texture + one whisper of pink ribbon. NO text, NO patterns on linen, NO additional props. Shot on Phase One IQ4, 100mm, f/3.5, ISO 100. WebP output 2560×1707.
```

### D1-05 — Stack of three blank cards with green clip · 4:5 vertical
```
Overhead-tight crop of three blank cream business cards (85mm × 55mm) loosely stacked but slightly fanned at the top edge, held by a single matte sage-green #8BC48A metal binder clip on the upper-left corner. The cards rest on a smooth off-white surface. Diffused overhead light, soft falloff to the sides. Color palette: cream cards + warm-cream surface + one sage-green clip. NO text, NO logos, NO printing on cards. Shot on Hasselblad H6D, 120mm macro, f/4, ISO 100. The mood is "ready to write, before the words arrive." WebP output 2048×2560.
```

**Slot mapping for HTML integration:**
- D1-01 → S13 letterhead photo-composite alt (notebook variant)
- D1-02 → S13 business card front photo-composite
- D1-03 → S13 letterhead primary photo-composite
- D1-04 → S13 brochure/folded-application photo-composite
- D1-05 → S13 stationery-stack photo-composite (new card or hero-of-applications)

---

## Series D2 — Audience (8-17 year-olds, faces allowed)

**Purpose:** Marketing-grade portraits showing the إدراك student — the kid who decided they "weren't smart" and then found their moment. Used as future website hero images, social-channel covers, and brochure interiors.

**Style register — LOCKED:**
Editorial-comic illustration in the lineage of **Adrian Tomine** (New Yorker covers — clean ink line + flat color + emotional restraint), **Tom Gauld** (The Guardian comic strips — minimal line + subtle wit + sophisticated palette), and **Christoph Niemann** (single-image conceptual illustration — bold simplification + ideas-first). NOT Disney/Marvel cartoon (too commercial), NOT children's-book painterly (too "for little kids" — kills teen audience), NOT anime/manga (too genre-specific). The illustration must read as **sophisticated comic for thinking kids and teens**, not "cute drawing for children."

**Hard discipline for D2:**
- **Confident ink linework** — single weight 2-3px line work, no sketchy/wobbly lines, no AI watercolor smudge, no airbrush, no 3D-render look.
- **Flat brand-color fills only** — pure `#FAF8F3` cream field + `#0D0D0D` ink line + ONE dominant brand color per illustration (`#FF69B4`/`#4FC3F7`/`#F5D03A`/`#E07840`/`#8BC48A`). Up to ONE secondary accent at small scale. Never gradients. Never shading via blending — only flat planes and (optionally) one halftone-dot or riso-grain texture overlay.
- **Halftone/riso option** — subtle dot-pattern or riso-misregistration texture allowed on the dominant color fill for "printed editorial comic" feel. Use sparingly.
- **No outline-eyes-with-pupils cartoon faces.** Faces are simplified: a line for the brow, two small dots or short lines for eyes, a single line for the mouth. Tom Gauld / Niemann-level simplification. NO Disney-style large round eyes with sparkle. NO anime mouths.
- **No school-uniform clichés.** Loose comfortable clothing, simplified shapes — a sweater is a rounded rectangle with one curve at the neckline, not a render of fabric.
- **NO cultural framing at all.** No hijab, no thobe, no calligraphy on walls, no Arabic-mosaic patterns, no traditional dress, no religious framing, no geographic markers (no Tira/Palestine/Levantine visual cues). The brand is universal learning, not Arab-culture learning. Kids in the illustrations are universal-young-person — could be in Tira, Tokyo, Toronto, or Tunis. Treat as you would for an Apple education ad.
- **No fist-pumps, no laughing-into-frame "joy."** Quiet breakthrough, quiet thought, quiet turn-of-head. The moment BEFORE understanding lands.
- **Composition reads RTL** — figure or action enters from the right when there's a directional motion.

**Format:** 5 illustrations. WebP. 2048×2560 (4:5) for verticals, 2560×1707 (3:2) for horizontals.

### D2-01 — The desk moment, yellow dominant · 4:5 vertical
```
Editorial-comic illustration, Adrian Tomine register. A side-profile view of an 11-year-old at a simple desk, drawn with confident 2-3px ink line on flat cream #FAF8F3 background. The kid sits in 3/4-back-profile (only the line of the cheek, ear, and back of head visible — face mostly turned away from viewer). Their head is tilted slightly UP from the page on the desk. They wear a flat-color yellow #F5D03A sweater, drawn as simplified shapes with no shading — just clean ink line defining the neckline, sleeves, and one wrinkle at the elbow. On the desk: one open book drawn as two simple cream rectangles with a single ink hairline down the spine (no text on pages). One pencil, drawn as a thin yellow line with an ink-black tip. Above the kid's head, suspended in the cream space at upper-right, a single small yellow lightning-bolt shape (~10% of frame height) — the brand's "moment" element, drawn flat with the same ink outline. No background room, no walls, no window — just the cream field. Subtle yellow halftone-dot pattern only inside the sweater shape, suggesting print texture. NO TEXT anywhere. NO additional characters. NO floor or ground line. Style references: Adrian Tomine "New Yorker" cover, Tom Gauld for The Guardian, Christoph Niemann conceptual illustration. WebP output 2048×2560.
```

### D2-02 — Hands writing, blue dominant · 4:5 vertical
```
Editorial-comic illustration, Tom Gauld register. Overhead-top-down view of a 15-year-old's hands writing in a notebook, drawn with confident 2-3px ink line on flat cream #FAF8F3 background. The hands are simplified — clean ink outlines, no knuckle detail, no fingernails drawn, no skin shading. Forearms enter from the lower-left and lower-right edges, sleeves of a sky-blue #4FC3F7 long-sleeve shirt drawn as flat color fills with single line at cuff. Hands hold a pencil mid-air over an open notebook — the pencil has just touched the page and drawn a single curving line (not a letter, not text, just an abstract ink curve, like the start of a thought). Notebook is two cream rectangles with subtle blue halftone-dot pattern fill at the page edges only. The single drawn curve on the page is the same sky-blue color. To the upper-right of the frame, a small floating speech-balloon-like cloud shape (drawn in flat sky-blue, simplified rounded form) suggests "a thought arriving" — but the balloon is empty, no text, no symbol. NO TEXT, NO logo. Style references: Tom Gauld minimal panel work, Adrian Tomine cropped editorial frames. WebP output 2048×2560.
```

### D2-03 — The window, green dominant · 4:5 vertical
```
Editorial-comic illustration, Christoph Niemann register. A 9-year-old kid stands at a tall window, drawn from the back — viewer sees the back of the head and shoulders, never the face. Confident 2-3px ink line on flat cream #FAF8F3 background. The kid is centered low in the frame (lower 40%), the upper 60% is the window — a tall vertical rectangle of slightly-darker cream tone with a single horizontal mullion line crossing it. The kid wears a sage-green #8BC48A t-shirt (flat color fill, no shading, simplified rounded shoulder shape) and dark grey trousers (drawn as flat darker-cream shape). In the kid's right hand, held loosely at their side: a small simplified notebook (cream rectangle with single ink-line spine). Outside the window, drawn as flat shapes: three abstract green tree-canopy curves at varying heights (simplified silhouettes, no leaf detail). A small sage-green stair-step shape (4 steps ascending, the brand's "growth" element) floats subtly in the lower-right corner of the window glass — like a thought hovering. NO TEXT, NO additional figures, NO ground line inside the room. Style references: Christoph Niemann "Sunday Sketch," Tom Gauld minimal landscape. WebP output 2048×2560.
```

### D2-04 — The turn, pink dominant · 4:5 vertical
```
Editorial-comic illustration, Adrian Tomine register with motion lines. A 16-year-old teen captured mid-turn, head and shoulders rotating from facing-away (camera-left) toward something off-frame to the camera-right. Drawn with confident 2-3px ink line on flat cream #FAF8F3 background. The teen wears a flat warm-pink #FF69B4 oversized sweatshirt (drawn as simplified rounded shape, no shading, one ink line at the hood seam). Face is shown in 3/4 profile partly turning — eye is a single short ink line (closed-blink mid-turn or downcast), mouth is one neutral horizontal line. Hair drawn as flat ink-black mass with 2-3 simple curving lines suggesting movement. Three short comic-style motion lines arc behind the head from camera-left, drawn in ink line (~5cm comic-motion-line marks), indicating the speed of the turn. To the camera-right at upper edge, a small pink arrow-shape (the brand's "drive" element, drawn flat with ink outline) floats — what they're turning toward. Subtle pink halftone-dot pattern inside the sweatshirt only. NO TEXT, NO floor, NO background room. Style references: Adrian Tomine "Killing and Dying" panel work, Tom Gauld with motion. WebP output 2048×2560.
```

### D2-05 — The conversation, orange dominant · 3:2 horizontal
```
Editorial-comic illustration, Tom Gauld register. Mid-shot from waist-level showing two figures across a small table, drawn with confident 2-3px ink line on flat cream #FAF8F3 background. The composition is profile-view — both figures shown from the side, viewer sees both in profile. On the camera-left: an adult (~40s, parent figure), drawn from chest-up in 3/4 profile, head slightly tilted toward the child opposite. Adult wears a flat warm-grey simple shirt (no shading). On the camera-right: a 12-year-old child, drawn slightly smaller in scale, head slightly tilted upward toward the parent. Child wears a flat orange #E07840 sweater. Between them on the table: one orange ceramic mug (simplified flat shape, single ink outline, gentle wisp of steam drawn as one ink curve rising). The table is drawn as a simple horizontal cream rectangle with one ink line on its near edge. Faces are SIMPLIFIED — single ink lines for closed-eye contemplation, neutral mouth lines (no smiles, no frowns — just calm). Subtle orange halftone-dot pattern inside the child's sweater only. NO TEXT, NO additional figures, NO background detail behind the table. Style references: Tom Gauld "Mooncop" intimate two-figure framing, Adrian Tomine quiet interiors. WebP output 2560×1707.
```

**Slot mapping for HTML integration:**
- D2-01 → Future S02 secondary panel ("the student who decided") OR new Section 17 (Audience)
- D2-02 → S04 student-voice panel background-image (composited with pink quote overlay)
- D2-03 → S04 parent-voice panel background-image (composited with blue quote overlay)
- D2-04 → Future website hero "the moment" alternate cover
- D2-05 → S04 hero or transition between voice columns

---

## Series #5 — The cinematic illustrated hero (single dramatic frame)

**Purpose:** One hero illustration that reads like a single iconic panel from a graphic novel — the visual climax of "the closed door opens." Used as alternate website hero, brand-book PDF cover-spread, social-share OpenGraph meta-image.

**Style register — same as D2:** Adrian Tomine + Tom Gauld + Christoph Niemann editorial-comic. Confident ink line + flat brand-color fills + optional halftone texture.

**Format:** 1 illustration. WebP. 2560×1707 (3:2) horizontal.

### #5-01 — The five elements in suspended composition · 3:2 horizontal
```
Editorial-comic illustration, Christoph Niemann conceptual register. A wide horizontal frame in confident 2-3px ink line on flat cream #FAF8F3 background. The composition shows the five brand elements suspended in cream space as if floating in a single moment of arrival — arranged with RTL leading (denser on the right, sparser on the left, suggesting motion entering the frame from the right). FIVE elements, each drawn flat with ink outline and brand-color fill, varying in scale: 1) UPPER-RIGHT, largest — a yellow #F5D03A lightning-bolt shape (the "moment" element, ~30% of frame height, drawn flat with subtle yellow halftone-dot fill); 2) MID-RIGHT, medium — a sage-green #8BC48A staircase shape (4-5 ascending steps, drawn flat, ~20% frame height); 3) CENTER — a sky-blue #4FC3F7 half-dome (the "clarity" element, ~25% frame height, flat fill); 4) MID-LEFT — a pink #FF69B4 forward-arrow (the "drive" element, ~15% frame height, pointing RIGHT into the composition); 5) LOWER-LEFT, smallest — an orange #E07840 spark/radiating-lines shape (~10% frame height). The elements sit at varied vertical heights to create visual rhythm — bolt high-right, dome center, spark low-left. A subtle ink-line connecting all five elements as a single curving path (drawn as one continuous 1px ink curve threading through them, like a constellation line) suggests they belong to one system. NO TEXT, NO LOGOS, NO ground plane, NO horizon, NO people, NO frame border. Subtle riso-print misregistration texture (a hint of 1-2px color offset on each fill) for "printed-comic-cover" authenticity. Style references: Christoph Niemann "Abstract Sunday," Adrian Tomine cover work, Tom Gauld panel composition. WebP output 2560×1707.
```

**Slot mapping for HTML integration:**
- #5-01 → Optional alternate hero (S01 variant), brand-book PDF cover-spread image, website OpenGraph meta image (1200×630 crop)

---

## Post-generation integration notes

1. **Save all WebPs to `C:\Projects\Idrak-Brand-System\assets\media\`** with names matching the slot:
   - D1 stays photographic: `d1-01-notebook.webp`, `d1-02-card.webp`, etc.
   - D2 is now illustration: `d2-01-illus-desk.webp`, `d2-02-illus-hands.webp`, etc.
   - #5 is now illustration: `hero-illus.webp`
2. **Verify discipline before committing:**
   - D1 — no people, no Arabic typeset, no cultural-tourism dressing (§13b Rule 15)
   - D2 + #5 — confident ink line, flat brand colors only, no gradient/shading, no Disney-eye cartoon faces, no Arabic-cultural framing, no text
3. **For D1 stationery composites:** image as CSS `background-image`, `logo-wordmark.svg` composited absolutely on top (§13b Rule 14).
4. **For D2 illustrations:** can be used three ways depending on slot —
   - As section background-image with brand-color quote overlay
   - As inline `<img>` artifact inside a section (S04 voice cards, future audience section)
   - As social-share / OpenGraph image at 1200×630 crop
   Test text contrast against the cream illustration field (WCAG AA min for any composited type).
5. **For #5 illustration hero:** test at 1440px AND mobile 375px. Crop-safe zone is the central 60% (the dome + bolt + arrow). The spark and stairs at the edges can crop safely on mobile.
6. **Reject criteria for D2 + #5 (illustration):** re-prompt if Nano Banana introduces — Disney-style round eyes with sparkles, watercolor/airbrush shading, photo-realistic faces, anime mouths, all 5 brand colors competing in one frame (D2 each has ONE dominant), any visible text, 3D-render look, vignettes, dramatic light beams, kawaii sweat-drops or speech-balloon symbols beyond what's specified, cultural-tourism props.
7. **Reject criteria for D1 (still photo):** any visible text on papers, AI-tell symmetry, all 5 colors at once, lens-flare, magic-hour orange light.

---

## Series E — Social banners (illustrated, quote-overlay zones)

**Decisions locked:** Tomine/Gauld/Niemann register. Generic universal-young-person. One dominant brand color per frame. D1 = 5 photos. #5 = 1 illustration.

**Purpose:** Illustrated social-media banners in the same editorial-comic register as D2. Each leaves a clear **quote-overlay zone** — a deliberately empty cream area designed so a brand quote in Cairo Arabic can be composited on top at production time.

**Quote zones:** Do NOT letter any text in the illustration itself. Instead, engineer the composition so the correct zone (noted per prompt) is pure flat cream `#FAF8F3` with no ink marks. This zone is where the developer composites the brand quote via CSS/HTML overlay.

**Format:** 5 illustrations. WebP. Square 1080×1080 (1:1), vertical 1080×1920 (9:16), horizontal 1200×628 (≈2:1).

**File-save naming:** `e-01-social-yellow.webp`, `e-02-social-pink.webp`, `e-03-stories-blue.webp`, `e-04-stories-orange.webp`, `e-05-linkedin-green.webp`

---

### E-01 — Instagram 1:1 · Yellow · "The moment" · quote zone lower-third

```
Editorial-comic illustration, Tomine/Niemann register. Square 1080×1080 frame. Flat cream #FAF8F3 background. Confident 2-3px ink line throughout.

COMPOSITION: A single 11-year-old kid sits cross-legged in the upper-center of the frame (upper 55%), drawn in 3/4-back-profile — head slightly tilted up, as if a thought just arrived. The kid wears a yellow #F5D03A sweater (flat color fill, simplified silhouette, subtle yellow halftone-dot texture inside the shape only). Hair drawn as flat ink-black mass with 3 loose curving strokes. No face visible — only the back of the head and the line of one cheek. To the upper-right of the kid's head, a single yellow #F5D03A lightning-bolt brand element (flat fill, ink outline, ~15% of frame height) hovers like a thought materialising. The bolt and the kid's head are the only two objects in the upper portion.

QUOTE ZONE: The lower 40% of the frame is pure flat cream — NO ink marks, no objects, no ground lines, completely empty. This is the text-overlay zone. Leave it entirely blank.

NO TEXT anywhere. NO floor. NO background walls. NO additional objects. Style: Adrian Tomine New Yorker cover restraint + Christoph Niemann conceptual simplicity. One-color illustration + ink line + cream only. WebP 1080×1080.
```

---

### E-02 — Instagram 1:1 · Pink · "The energy" · quote zone left-third

```
Editorial-comic illustration, Tom Gauld register. Square 1080×1080 frame. Flat cream #FAF8F3 background. Confident 2-3px ink line throughout.

COMPOSITION: Three simplified pink #FF69B4 forward-arrow shapes (the brand's "arrows/drive" element) are arranged in a diagonal cluster entering from the camera-right edge, pointing leftward into the frame — each arrow drawn as a flat filled shape with ink outline, slightly varying in scale (largest at upper-right, smallest at lower-center-right). The arrows occupy the right 55% of the frame. A single 14-year-old teen figure, drawn from the waist up, faces right (the direction the arrows point), standing in the center-right of the frame. Figure is simplified — flat pink oversized hoodie, head drawn as ink oval with minimal features (one line for brow, two dots for eyes, single neutral line for mouth). Subtle pink halftone-dot texture inside the hoodie only.

QUOTE ZONE: The left 40% of the frame is pure flat cream — no arrows, no figure, no ink marks. Completely empty. This is the text-overlay zone.

NO TEXT anywhere. NO background. NO floor line. Style: Tom Gauld Guardian strips + Adrian Tomine cropped panels. WebP 1080×1080.
```

---

### E-03 — Instagram Stories 9:16 · Blue · "The clarity" · quote zone center-strip

```
Editorial-comic illustration, Christoph Niemann register. Tall vertical 1080×1920 frame. Flat cream #FAF8F3 background. Confident 2-3px ink line throughout.

COMPOSITION: The frame is divided into three natural zones — top, center, bottom — with the brand architecture:

TOP ZONE (upper 30%): A large sky-blue #4FC3F7 half-dome shape (the "clarity" element) arcs from the upper-left to upper-right edge, filling the top zone like a header. The dome is a flat fill with ink outline, no interior detail. The dome's flat edge faces downward toward the center.

BOTTOM ZONE (lower 25%): A simplified 9-year-old kid figure stands centered, drawn from the waist up, back to the viewer. Wears a sky-blue #4FC3F7 t-shirt (flat fill, simplified shape). Hands at sides. Looking upward toward the dome. Figure drawn with confident ink line, simplified silhouette.

QUOTE ZONE (center 45%): Pure flat cream — no marks, no objects, completely empty strip between the dome and the figure. This is the text-overlay zone.

NO TEXT. NO ground line. NO background detail. Style: Christoph Niemann abstract Sunday + Tom Gauld minimal landscape. WebP 1080×1920.
```

---

### E-04 — Instagram Stories 9:16 · Orange · "The drive" · quote zone upper-center

```
Editorial-comic illustration, Adrian Tomine register. Tall vertical 1080×1920 frame. Flat cream #FAF8F3 background. Confident 2-3px ink line throughout.

COMPOSITION:

BOTTOM ZONE (lower 40%): A 15-year-old teen figure, drawn from the mid-chest down, seated at a simple desk — only the torso and hands visible, no head in frame. The teen wears an orange #E07840 sweater (flat fill, halftone-dot texture inside only). Both hands rest on the desk surface, one hand holding a pencil above a blank notebook page (cream rectangle with single spine line — no text). The desk edge is one ink line.

TOP ZONE (upper 30%): An orange #E07840 spark/radiating-lines shape (the brand's "energy" element, ~20% of frame height) sits centered at the very top of the frame, like an arriving idea.

QUOTE ZONE (center 30%): Pure flat cream — completely empty between the figure's head area and the spark above. This is the text-overlay zone.

NO TEXT. Style: Adrian Tomine cropped intimate frames + Tom Gauld quiet moments. WebP 1080×1920.
```

---

### E-05 — LinkedIn 2:1 · Green · "The growth" · quote zone right-half

```
Editorial-comic illustration, Tom Gauld register. Wide horizontal 1200×628 frame. Flat cream #FAF8F3 background. Confident 2-3px ink line throughout.

COMPOSITION: The illustration occupies the LEFT HALF of the frame only (left 50%).

LEFT HALF: A sage-green #8BC48A staircase shape (5 ascending steps, the brand's "growth" element) rises from the lower-left corner toward the upper-center. The stairs are drawn as flat color fill with ink outline, each step a clean rectangle. A small simplified figure (12-year-old kid, drawn as a flat ink silhouette, ~8% of frame height) stands at the top of the staircase facing right — simplified into: oval head, rectangular body in sage-green sweater, two short lines for legs. The figure looks toward the right half of the frame. A thin green vertical tick-ladder (5 thin horizontal lines at equal intervals along a 1px ink vertical) runs up the far-left edge, echoing the steps.

QUOTE ZONE: The right 50% of the frame is pure flat cream — completely empty. This is the text-overlay zone.

NO TEXT. NO background. Style: Tom Gauld "Mooncop" wide-panel restraint + Niemann conceptual negative space. WebP 1200×628.
```

---

**Slot mapping for Series E:**
- E-01 → Instagram feed post (quote: `نأخذ كل طالب إلى لحظة إدراكه.`)
- E-02 → Instagram feed post — student-voice (quote: `أنت لست المشكلة`)
- E-03 → Instagram Story frame 1 — clarity/calm (quote: `الهدوء ما بعد العاصفة`)
- E-04 → Instagram Story frame 2 — drive/desk (quote: `لا نزيد الجهد.. بل نمنح العقل أدواته`)
- E-05 → LinkedIn banner (quote: `مسارٌ جديد للفهم`)

---

## Decisions locked (2026-05-22)

- D2 style: **Tomine/Gauld/Niemann register** as written — quiet, editorial, sophisticated
- D2 characters: **Generic universal-young-person** — no specific builds
- D1 stationery: **5 photos** — fire as-is
- Hero #5: **One illustration** — fire as-is
- Series E: **Added above** — 5 social banners

**LOCKED — do not ask again:** No cultural framing, no hijab, no traditional dress, no geographic markers. Universal-learning-brand globally.
