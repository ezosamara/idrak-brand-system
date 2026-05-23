# COPY.md — إدراك Brand Book

**Every piece of visible text in the book, in reading order, bilingual pairs.**
Hand this to the copywriter. Each block shows the current Arabic + English exactly as it ships, plus a `WHERE` note so the rewrite can be dropped back into `index.html` precisely.

Notes for the copywriter:
- Arabic and English do NOT have to be literal translations. They should each carry the same meaning with the right tone in their own language.
- **DO NOT rewrite** anything inside an `🔒 LOCKED` block — these are Raya's words (CLAUDE.md §10) and the brand is built around them.
- **Eyebrows** (the small caps Lato labels like "MISSION · الرسالة") should stay short — max 3–4 words each side.
- **Display headlines** can run 2 lines, max ~60 Arabic characters / ~50 Latin characters per line.
- Section counters (`01 / 15`, `02 / 15` …) are SYSTEM — do not rewrite.
- `إدراك` always means the brand name. Keep it un-translated inside English copy where it appears.

---

## SECTION 01 — Cover (Hero)

**WHERE:** `<section id="s01">` — full-bleed cover, layered brand elements behind the logo SVG.

| Slot | Current text | Type |
|---|---|---|
| Vertical spine (RTL leading edge) | `BRAND IDENTITY · 01 / 15 · EDITION 01 · 2026` | English caps, single line, written vertically |
| Folio number (top-left) | `01` | System counter — leave |
| Folio label | `الغلاف` · `Cover` | bilingual chip |
| Foot — English | `Smart Learning Center · Tira` | tagline |
| Foot — Arabic | `مركز التعلّم الذكي · طيرة` | tagline |

---

## SECTION 02 — Brand Story

**WHERE:** `<section id="s02">` — right column anchors the Arabic mission; left column bleeds the bolt.

| Slot | Current text |
|---|---|
| Chrome — English | `02 · Brand Story` |
| Chrome — Arabic | `القصة` |
| Eyebrow | `الرسالة · Mission` |
| Headline — Arabic 🔒 LOCKED | `نأخذ كل طالب`<br>`إلى لحظة إدراكه.` |
| Headline — English | `We take every student to their moment of إدراك — whatever their starting point, whatever the path.` |
| Beat 1 — Arabic 🔒 LOCKED | `اثنتا عشرة سنة في الميدان علّمتنا شيئاً واحداً: الطالب الذي يُقال عنه "ما بيفهم" — لم يفشل في التعلّم. فشل النظام في أن يجد بابه.` |
| Beat 2 — Arabic 🔒 LOCKED | `إدراك وُلد من هذا الإيمان. نحن لا نُدرّس مناهج — نبني خططاً. خطة لكل طالب بمفرده، تبدأ بتشخيص حقيقي لطريقة تفكيره.` |
| Beat 3 — Arabic 🔒 LOCKED | `أدواتنا تختلف: استراتيجيات تعليمية، تعلّم من خلال اللعب، وجلسات neurofeedback. لكن الهدف واحد — أن يخرج الطالب واثقاً لا لأنه نجح في الامتحان، بل لأنه فهم كيف يُفكّر.` |
| Beat 4 (final, larger) — Arabic 🔒 LOCKED | `لا نعيد سرد الدروس.. بل نصنع لحظة إدراك` |
| Punctum tag — English | `اللحظة · The moment` |
| Punctum tag — Arabic | `الومضة التي يولد بها الإدراك — البرق الذي يُشرع الباب.` |
| Foot — left | `قصة إدراك` · `Twelve years · one belief · one door` |
| Foot — right | `02 · القصة` |

Copywriter note: the four LOCKED beats above are direct from Raya. **Do not paraphrase.** The English beats can be added as a parallel sub-translation if you want — currently there is only the English headline + Arabic beats.

---

## SECTION 03 — Brand DNA (5 pillars)

**WHERE:** `<section id="s03">` — 5 stacked scenes, one per brand colour.

Repeating chrome on every pillar:
- `03 · Brand DNA` / `حمض الهوية`
- Pillar counter `NN / 05` and `DNA · Brand Pillars`

### Pillar 01 · Yellow · اللحظة
| Slot | Text |
|---|---|
| Tag | `#F5D03A · YELLOW · اللحظة` |
| Eyebrow | `Pillar 01 · The Moment · اللحظة` |
| Arabic name (display) | `اللحظة` |
| English name | `The Moment` |
| Description (English) | `The lightbulb. The exact moment the word falls into place. Hot, charged, impossible to ignore. *The colour of إدراك itself.*` |

### Pillar 02 · Orange · الاندفاع
| Slot | Text |
|---|---|
| Tag | `#E07840 · ORANGE · الاندفاع` |
| Eyebrow | `Pillar 02 · The Drive · الاندفاع` |
| Arabic name | `الاندفاع` |
| English name | `The Drive` |
| Description | `The moment before breakthrough. *Inner fire that refuses to surrender.* Energy accent, motion elements, the path before the result.` |

### Pillar 03 · Pink · الطاقة
| Slot | Text |
|---|---|
| Tag | `#FF69B4 · PINK · الطاقة` |
| Eyebrow | `Pillar 03 · The Energy · الطاقة` |
| Arabic name | `الطاقة` |
| English name | `The Energy` |
| Description | `*The student's voice.* Courage to try again after failure. Small celebrations. All student-facing communication.` |

### Pillar 04 · Blue · الوضوح
| Slot | Text |
|---|---|
| Tag | `#4FC3F7 · BLUE · الوضوح` |
| Eyebrow | `Pillar 04 · The Clarity · الوضوح` |
| Arabic name | `الوضوح` |
| English name | `The Clarity` |
| Description | `After understanding — clarity. *Directly tied to neurofeedback:* training the mind toward calm focus. Parent voice, information, cognitive content.` |

### Pillar 05 · Green · النمو
| Slot | Text |
|---|---|
| Tag | `#8BC48A · GREEN · النمو` |
| Eyebrow | `Pillar 05 · The Growth · النمو` |
| Arabic name | `النمو` |
| English name | `The Growth` |
| Description | `Patience that bears fruit. *Slow and certain*, like self-confidence. Step motif, progress content, treatment journey.` |

Copywriter note: each description should run 1–2 sentences max. Italicised phrase is the brand-belief line — keep it tight, declarative.

---

## SECTION 04 — Two Voices

**WHERE:** `<section id="s04">` — split column, parent (blue) on physical right, student (pink) on physical left.

| Slot | Text |
|---|---|
| Chrome — English | `04 · Two Voices` |
| Chrome — Arabic | `صوتان · لمن نعمل` |

### Parent column (right, blue, dome)
| Slot | Text |
|---|---|
| Eyebrow | `Voice 01 · Parent · للوالد` |
| Arabic name | `للوالد` |
| English name | `For the Parent` |
| Arabic quote 🔒 LOCKED | `الذي جرّب كل شيء ولم يرَ فرقاً.` |
| English quote | `…who tried everything and saw no difference.` |

### Student column (left, pink, arrows)
| Slot | Text |
|---|---|
| Eyebrow | `Voice 02 · Student · للطالب` |
| Arabic name | `للطالب` |
| English name | `For the Student` |
| Arabic quote 🔒 LOCKED | `الذي أقنع نفسه أنه «مش ذكي».` |
| English quote | `…who convinced himself he is "not smart."` |

Foot: `Audience · Voices` and `Two Voices · صوتان`

---

## SECTION 05 — Colour System (6 full-bleed scenes)

**WHERE:** `<section id="s05">` — 6 stacked full-bleed colour takeovers.

Repeating chrome: `05 · Colour System` / `النظام اللوني` + per-scene counter `NN / 06`.

### Scene 01 · Ink · الحبري · الأساس
| Slot | Text |
|---|---|
| Eyebrow | `Pillar 01 · #0D0D0D · INK` |
| Arabic name (display) | `الحبري` |
| Sub-pillar | `الأساس · The Foundation` |
| Story | `*The weight before understanding.* Certainty — when a student reaches their answer, they write it here.` |
| Usage | `Logo · Headlines · Structure` |

### Scene 02 · Yellow · الأصفر · اللحظة
| Eyebrow | `Pillar 02 · #F5D03A · YELLOW` |
| Display | `الأصفر` |
| Sub-pillar | `اللحظة · The Moment` |
| Story | `The lightbulb. *The exact moment the word falls into place.* Hot, charged, impossible to ignore. The colour of إدراك itself.` |
| Usage | `Aha moments · Spark element · Punctum` |

### Scene 03 · Blue · السماوي · الوضوح
| Eyebrow | `Pillar 03 · #4FC3F7 · BLUE` |
| Display | `السماوي` |
| Sub-pillar | `الوضوح · The Clarity` |
| Story | `After understanding — clarity. *Directly tied to neurofeedback:* training the mind toward calm focus.` |
| Usage | `Parent voice · Information · Cognitive content` |

### Scene 04 · Orange · البرتقالي · الاندفاع
| Eyebrow | `Pillar 04 · #E07840 · ORANGE` |
| Display | `البرتقالي` |
| Sub-pillar | `الاندفاع · The Drive` |
| Story | `The moment before breakthrough. *Inner fire that refuses to surrender.* The path before the result.` |
| Usage | `Energy accent · Motion elements · Direction` |

### Scene 05 · Pink · الوردي · الطاقة
| Eyebrow | `Pillar 05 · #FF69B4 · PINK` |
| Display | `الوردي` |
| Sub-pillar | `الطاقة · The Energy` |
| Story | `*The student's voice.* Courage to try again after failure. Small celebrations.` |
| Usage | `Student-facing comms · Social · Celebrations` |

### Scene 06 · Green · الأخضر · النمو
| Eyebrow | `Pillar 06 · #8BC48A · GREEN` |
| Display | `الأخضر` |
| Sub-pillar | `النمو · The Growth` |
| Story | `Patience that bears fruit. *Slow and certain*, like self-confidence.` |
| Usage | `Step motif · Progress content · Treatment journey` |

---

## SECTION 06 — Typography

**WHERE:** `<section id="s06">` — bilingual specimen spread (Lato | Cairo).

| Slot | Text |
|---|---|
| Chrome | `06 · Typography` / `النظام الطباعي` |

### Latin column (Lato)
| Row | Spec | Specimen text |
|---|---|---|
| Display | `96 / 900` | `The Moment` |
| H1 | `64 / 700` | `We don't teach — we open the door.` |
| H2 | `38 / 600` | `We take every student to their moment of إدراك.` |
| Body | `17 / 400` | `Twelve years in the field taught us one thing: the student labelled "doesn't understand" didn't fail at learning. The system failed to find their door.` |
| Eyebrow | `11 / 400` | `Smart Learning Center · Tira` |

### Arabic column (Cairo)
| Row | Spec | Specimen text |
|---|---|---|
| Display | `96 / 900` | `اللحظة` |
| H1 | `64 / 700` | `لا نعيد سرد الدروس.. بل نصنع لحظة إدراك` |
| H2 | `38 / 600` | `نأخذ كل طالب إلى لحظة إدراكه.` |
| Body | `17 / 400` | `اثنتا عشرة سنة في الميدان علّمتنا شيئاً واحداً: الطالب الذي يُقال عنه "ما بيفهم" — لم يفشل في التعلّم. فشل النظام في أن يجد بابه.` |
| Eyebrow | `13 / 400` | `مركز التعلّم الذكي · طيرة` |

Foot:
- `Latin · Lato · 300 / 400 / 700`
- `Arabic · Cairo · 300 / 400 / 500 / 600 / 700 / 900`

Copywriter note: the body row in both columns is the same Beat 1 / paragraph 1 from S02 — keep them aligned in meaning if S02 is rewritten.

---

## SECTION 07 — Elements

**WHERE:** `<section id="s07">` — 5-card vocabulary grid.

Chrome: `07 · Elements` / `العناصر`

| Card | Tag | Arabic name | English name | Usage line |
|---|---|---|---|---|
| 01 | `Yellow · #F5D03A` | `اللحظة` | `The Moment` | `The lightbulb. Aha moments, spark punctum.` |
| 02 | `Orange · #E07840` | `الاندفاع` | `The Drive` | `Ignition, the moment of contact. Motion accent.` |
| 03 | `Pink · #FF69B4` | `الطاقة` | `The Energy` | `Forward motion, the student's voice.` |
| 04 | `Blue · #4FC3F7` | `الوضوح` | `The Clarity` | `Clarity, the dome of the answer. Parent voice.` |
| 05 | `Green · #8BC48A` | `النمو` | `The Growth` | `The learning journey. Patience that bears fruit.` |

Foot: `Vocabulary · 5 elements · 5 colors · 5 brand stories` and `Specimen · ورقة العناصر`

---

## SECTION 08 — Logo Variations

**WHERE:** `<section id="s08">` — 3-card grid.

Chrome: `08 · Logo Variations` / `صيغ الشعار`

| Card | Tag | Arabic name | English name | Use line |
|---|---|---|---|---|
| 01 | `Variation 01 · Primary` | `الشعار المطلق` | `Primary Wordmark` | `Default mark. Every section header, every signature, every application.` |
| 02 | `Variation 02 · With Tagline` | `مع الوصف` | `With Tagline` | `Use where the brand needs context: first-touch surfaces, business cards, intro pages.` |
| 03 | `Variation 03 · With Rays` | `مع الإشعاع` | `With Rays` | `Celebratory lockup. Reserved for hero moments — campaign opens, milestone announcements.` |

Foot: `Sacred · Always <img src> · Never trace, never recreate` and `Three files only · ٣ صيغ فقط`

---

## SECTION 09 — Logo Anatomy

**WHERE:** `<section id="s09">` — square diagram with 6 labels outside the frame.

| Slot | Text |
|---|---|
| Chrome | `09 · Logo Anatomy` / `تشريح الشعار` |
| Eyebrow | `Reference · Anatomy` |
| Headline — Arabic | `الشعار يُرسم — ولا يُطبع` |
| Headline — English | `The mark is drawn, not typeset. These measurements exist so you can recognise it — never to reconstruct it.` |

### 6 callout labels (each = num + Arabic + English)
| # | Num | Arabic | English |
|---|---|---|---|
| 1 | `A-01` | `خط الذروة` | `Cap Line` |
| 2 | `A-02` | `القمة الحادة` | `Spike Apex` |
| 3 | `A-03` | `نقطة الارتكاز` | `Anchor Point` |
| 4 | `A-04` | `الكتلة الرئيسية` | `Primary Mass` |
| 5 | `A-05` | `خط القاعدة` | `Baseline` |
| 6 | `A-06` | `التباعد البصري` | `Optical Spacing` |

Foot: `Reference only · Anatomy is observed, not redrawn` and `Never reconstruct the mark · لا يُعاد بناء الشعار`

---

## SECTION 10 — Clear Space

**WHERE:** `<section id="s10">` — clearance diagram + 3-item legend.

| Slot | Text |
|---|---|
| Chrome | `10 · Clear Space` / `المساحة الآمنة` |
| Eyebrow | `Reference · Clear Space` |
| Headline — Arabic | `مساحة الشعار مقدسة` |
| Headline — English | `The mark needs room to breathe. Keep a minimum of one unit (x) on every side — clear of type, image, edge, or other graphics.` |

### Legend
| Num | Arabic | English |
|---|---|---|
| `1x` | `الحد الأدنى` | `Minimum clear space on every side. Never less.` |
| `2x` | `المُفضّل` | `Preferred on covers, hero panels, signage — wherever the brand leads.` |
| `x` | `وحدة القياس` | `Equals the cap-height of the wordmark's anchor glyph. Scales with the mark.` |

Foot: `The rule · No type, image, or graphic enters the dashed zone` and `No exceptions · دون استثناء`

---

## SECTION 11 — Logo on Backgrounds

**WHERE:** `<section id="s11">` — 7 surfaces + rule card.

| Slot | Text |
|---|---|
| Chrome | `11 · Logo on Backgrounds` / `الشعار على الخلفيات` |
| Eyebrow | `Reference · Surfaces` |
| Headline — Arabic | `حضور صلب على كل خلفية` |
| Headline — English | `The mark keeps full contrast on every approved surface. Ink wordmark on light fields, white wordmark on colour fields and ink. No grey, no tinted, no outlined versions.` |

### Surface cards (each = name + hex + logo-treatment rule)
| # | Arabic name | English name + hex | Rule |
|---|---|---|---|
| 1 | `الحبري` | `Ink · #0D0D0D` | `White logo` |
| 2 | `الكريمي` | `Cream · #FAF8F3` | `Ink logo` |
| 3 | `الوردي` | `Pink · #FF69B4` | `White logo` |
| 4 | `السماوي` | `Blue · #4FC3F7` | `White logo` |
| 5 | `الأصفر` | `Yellow · #F5D03A` | `Ink logo` |
| 6 | `البرتقالي` | `Orange · #E07840` | `White logo` |
| 7 | `الأخضر` | `Green · #8BC48A` | `White logo` |

### Rule card (8th card)
| Slot | Text |
|---|---|
| Number | `2` |
| Arabic rule | `قاعدتان فقط — أبيض على الداكن، حبري على الفاتح` |
| English rule | `Two rules only. White on dark or saturated fields. Ink on cream and yellow. Never anything else.` |

Foot: `Sacred mark · White via CSS filter only · no new SVG` and `Seven surfaces · ٧ خلفيات معتمدة`

---

## SECTION 12 — Logo Misuse

**WHERE:** `<section id="s12">` — 6-card forbidden grid (each card stamped with X).

| Slot | Text |
|---|---|
| Chrome | `12 · Logo Misuse` / `الاستخدام الخاطئ` |
| Eyebrow | `Reference · Misuse` |
| Headline — Arabic | `الشعار كيان مغلق — يُمنع المساس به` |
| Headline — English | `Never modify the mark. The wordmark ships as one of three sacred SVGs. Stretching, rotating, recolouring, restyling, or recreating the mark is forbidden — without exception.` |

### Misuse cards (each = tag + Arabic rule + English rule)
| # | Tag | Arabic rule | English rule |
|---|---|---|---|
| 1 | `Misuse 01 · لا` | `يُمنع تشويه أو مط أو ضغط هندسة الشعار` | `Never stretch, squash, or scale non-uniformly.` |
| 2 | `Misuse 02 · لا` | `يُمنع تدويره — الشعار يستقر أفقياً وبثبات تام` | `Never rotate at any angle. The mark always sits upright.` |
| 3 | `Misuse 03 · لا` | `يُمنع تطبيق ألوان غير معتمدة أو طبقات شفافة` | `Ink or white only. Never tinted, never recoloured.` |
| 4 | `Misuse 04 · لا` | `يُمنع إضافة ظلال أو توهج أو عمق مصطنع` | `No shadows, glows, outlines, or 3D effects. Ever.` |
| 5 | `Misuse 05 · لا` | `يُمنع وضعه فوق خامات معقدة أو صور مزدحمة` | `Never place on busy surfaces, patterns, or low-contrast fields.` |
| 6 | `Misuse 06 · لا` | `يُمنع استبدال الشعار المرسوم بخطوط طباعية عادية` | `Never re-typeset the brand word. The logo is a drawn SVG — not text.` |

Foot: `Sacred mark · Three SVGs only · never modified` and `No exceptions · دون استثناء`

---

## SECTION 13 — Applications

**WHERE:** `<section id="s13">` — hero campaign + 3 specimens (IG story · business card · letterhead).

| Slot | Text |
|---|---|
| Chrome | `13 · Applications` / `التطبيقات` |
| Eyebrow | `In the world · Applications` |
| Headline — Arabic | `الهوية في الميدان — تتحدث بوضوح وثبات` |
| Headline — English | `Real surfaces. Real copy. Each application carries the same discipline: one brand colour, one paired element, the sacred logo, and Raya's words.` |

### Spec 01 — Campaign Banner (pink, student voice)
| Slot | Text |
|---|---|
| Eyebrow on banner | `حملة · Student campaign` |
| Hero quote — Arabic 🔒 LOCKED | `نأخذ كل طالب`<br>`إلى لحظة إدراكه.` |
| Hero quote — English | `We take every student to their moment of understanding — whatever their starting point, whatever the path.` |
| Meta | `Spec 01 · Campaign Banner · Student voice` |
| Meta — Arabic | `حملة الطالب · 1600 × 700` |

### Spec 02 — Instagram Story (blue, parent voice)
| Slot | Text |
|---|---|
| Tag | `للوالد · For the parent` |
| Headline 🔒 LOCKED | `للوالد الذي جرّب كل شيء — ولم يرَ فرقاً` |
| Meta | `Spec 02 · Instagram Story · Parent voice` |
| Meta — Arabic | `قصة · 9:16` |

### Spec 03 — Business Card (cream, green accent)
| Slot | Text |
|---|---|
| Name | `راية عبد الحي` |
| Role | `Founder · Director` |
| Address line 1 | `مركز التعلّم الذكي` |
| Address line 2 | `طيرة المثلث` |
| Meta | `Spec 03 · Business Card · Cream` |
| Meta — Arabic | `بطاقة · 55 × 85` |

### Spec 04 — Letterhead (cream, orange watermark)
| Slot | Text |
|---|---|
| Date | `2026 / 05 / 21` |
| Salutation | `إلى ولي الأمر،` |
| Body paragraph | `نضع بين أيديكم مسار طفلكم للفصل القادم. لكل طالب بابه الخاص نحو الإدراك — وهذه الخطة صُممت لتخاطب ذكاءه، لا لتُصلح نقصه.` |
| Sign-off | `— فريق إدراك` |
| Meta | `Spec 04 · Letterhead · A4 Header` |
| Meta — Arabic | `رسالة · A4` |

Foot: `One discipline · One colour · one element · one mark per surface` and `Four specimens · ٤ نماذج`

Copywriter note: this section is the showcase. The hero quote is Raya's locked mission line. The other specimens can have their copy rewritten freely — they're meant to demonstrate brand voice in real surfaces.

---

## SECTION 14 — Motion Demo

**WHERE:** `<section id="s14">` — 4-card live primitive grid.

| Slot | Text |
|---|---|
| Chrome | `14 · Motion Demo` / `الحركة` |
| Eyebrow | `Live · Motion language` |
| Headline — Arabic | `الحركة لغة — لكل عنصر طريقته في الدخول` |
| Headline — English | `Motion is meaning. Four primitives carry the entire system. Each one matches a kind of arrival: text reveals, content rises, lines draw, presence breathes.` |

### 4 primitive cards
| # | Num | Arabic | English | Spec (technical) |
|---|---|---|---|---|
| 1 | `Primitive 01` | `الكشف` | `Reveal` | `0.6s · clip-path` |
| 2 | `Primitive 02` | `الصعود` | `Rise` | `0.5s · translateY` |
| 3 | `Primitive 03` | `الرسم` | `Draw` | `1.0s · dashoffset` |
| 4 | `Primitive 04` | `النَفَس` | `Loop` | `3.4s · infinite` |

Foot: `Easing · cubic-bezier(0.16, 1, 0.3, 1) · never linear` and `Four primitives only · ٤ حركات`

Copywriter note: the technical spec column is for engineers — leave the timing + property tokens as-is.

---

## SECTION 15 — Closing

**WHERE:** `<section id="s15">` — yellow takeover, mic-drop quote, signature, contact band.

| Slot | Text |
|---|---|
| Chrome | `15 · Closing` / `الخاتمة` |
| Eyebrow | `The moment · اللحظة` |
| Mic-drop quote — Arabic 🔒 LOCKED | `لا نعيد سرد الدروس.. بل نصنع لحظة `*`إدراك`* |
| Quote — English | `We do not teach. We bring students into understanding — into the exact moment the word falls into place.` |
| Thanks — Arabic | `شكراً` |
| Thanks — English | `Thank you · إدراك Brand Book 2026` |

### Contact band (4 cells)
| Label | Value |
|---|---|
| `Center · المركز` | `مركز التعلّم الذكي` |
| `Location · الموقع` | `طيرة المثلث` |
| `Instagram` | `@idrak.center` |
| `Founder · المؤسِّسة` | `راية عبد الحي` |

Foot: `End · إدراك · Smart Learning Center · Tira` and `15 / 15 · نهاية`

---

## Locked phrases — the spine of the brand

These appear multiple times. **DO NOT rewrite. Period.** All from Raya, CLAUDE.md §10.

| Phrase | Where it appears |
|---|---|
| `نأخذ كل طالب إلى لحظة إدراكه.` | S02 headline · S06 type spec · S13 hero quote |
| `لا نعيد سرد الدروس.. بل نصنع لحظة إدراك` | S02 final beat · S06 type spec · S15 mic-drop |
| `للوالد الذي جرّب كل شيء — ولم يرَ فرقاً.` | S04 parent quote · S13 IG story |
| `الذي أقنع نفسه أنه «مش ذكي».` | S04 student quote |
| The four S02 beats | S02 only |

The English equivalents of these phrases can be re-written — but the meaning must stay intact.

---

## What I need back from the copywriter

1. A revised version of this document with each `Current text` cell replaced.
2. Word-count flag if any rewrite exceeds the original by more than ~20% — display headlines and eyebrows have layout-fixed slots.
3. Any new phrases you want to add (extra eyebrows, captions, signage) — note the section + slot.

Once the rewrite is back, I'll diff it into `index.html` section-by-section and re-screenshot.
