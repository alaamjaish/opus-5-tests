# اختبار Opus 5 

> البرومبتات الكاملة التي استخدمتها لاختبار نموذج **Opus 5** ليلة إطلاقه، وكم كلّف كل واحد منها.
> *The seven verbatim prompts used to stress-test Opus 5 on release night, with the real cost of each.*

— [AlaaLab](https://alaalab.com)

---

## البناءات السبعة والتكلفة

| # | البناء | النوع | التكلفة |
|---|---|---|---:|
| ١ | [محاكاة القماش](#١--محاكاة-القماش) | بصري | $12.86 |
| ٢ | [TERRA · الأرض ثلاثية الأبعاد](#٢--terra--الأرض-ثلاثية-الأبعاد) | بصري | $25.67 |
| ٣ | [سطح مكتب ويندوز ٩٥](#٣--سطح-مكتب-ويندوز-٩٥) | بصري | $52.93 |
| ٤ | [Opus 5 يكتب عن نفسه](#٤--opus-5-يكتب-عن-نفسه) | بصري | $81.76 |
| ٥ | [حوض السمك الحيّ](#٥--حوض-السمك-الحيّ) | بصري | $56.90 |
| ٦ | [متحف الفن الإسلامي](#٦--متحف-الفن-الإسلامي) | بصري | $45.71 |
| ٧ | [مذكرة استثمارية عن Apple](#٧--مذكرة-استثمارية-عن-apple) | عمل معرفي | ≈ $31.64 * |
| | **المجموع** | | **≈ $307** |

---


## ١ — محاكاة القماش

قطعة قماش معلّقة تُحاكى كشبكة كتل ونوابض بتكامل Verlet، مثبّتة من الزاويتين العلويتين، مع جاذبية ورياح قابلة للضبط. تدور الكاميرا حولها، تسحب القماش بالمؤشر، و**تمزّقه** — والتمزّق ينتشر كما يفشل القماش الحقيقي لا كمربّعات نظيفة تختفي.

**شرط التمزّق هو الاختبار الحقيقي.** التنفيذ الساذج يحذف المربّعات؛ الفشل الحقيقي ينتشر على خطوط الإجهاد.

**التكلفة: $12.86** — الأرخص في الدفعة.

```
Build a 3D cloth simulation in a single runnable HTML file using three.js from a CDN.

A hanging cloth as a mass-spring grid with Verlet integration, pinned at the top corners, with gravity and adjustable wind making it billow.

Orbit the camera with the mouse. Grab and drag the cloth with the pointer. Tear it by dragging through it — the tears should propagate the way real fabric fails, not disappear in clean squares.

Soft lighting and a ground plane so the shadows and folds read as real. Sliders for wind, gravity, and stiffness, plus reset.

Loads efficiently, 60fps, no bundled asset files. One runnable HTML file.
put it in b projects — here we go bud!
```

---

## ٢ — TERRA · الأرض ثلاثية الأبعاد

كرة أرضية واقعية بصور NASA الحقيقية — خريطة Blue Marble النهارية، أضواء المدن الليلية، طبقة سحب، وخريطة نتوءات. تدوّرها وتقرّب من عمق الفضاء حتى سطح الأرض، مع خط فاصل بين الليل والنهار يتوهّج جانبه المظلم بأضواء المدن. ثلاثة أوضاع: قمر صناعي، أضواء ليلية، وخريطة سياسية قابلة للنقر.

**التكلفة: $25.67**

```
Build an interactive 3D Earth in a single runnable HTML file using three.js from a CDN.

Load real Earth textures from a public CDN URL: NASA Blue Marble day map, a night-lights map, a cloud layer, and a normal/bump map.

A realistic globe: spin it with the mouse and zoom smoothly from deep space right down close to the surface. A day/night terminator — the sunlit side shows the day map, the dark side glows with real city lights. Slowly drifting clouds and a soft blue atmosphere glow on the rim.

A control panel to SWITCH modes: satellite (day), night lights, and a political map with country borders. Make the countries clickable — clicking one highlights it and shows its name.

Sliders for rotation speed, cloud opacity, and sun position. 60fps. One runnable HTML file.
put it in b projects.
/effort max
```

---

## ٣ — سطح مكتب ويندوز ٩٥

سطح مكتب ويندوز ٩٥ يعمل فعلًا داخل ملف HTML واحد: قائمة ابدأ، شريط المهام، نوافذ تُسحب ويُغيَّر حجمها، Notepad وPaint، وMinesweeper تُلعب فعلًا. يُقلِع إقلاعًا كاملًا — شاشة POST ثم شاشة البداية ثم سطح المكتب — ونغمة الإقلاع **مُولَّدة في Web Audio لحظة سماعها**، لا محمّلة من ملف.

**القيد هو ما يجعله اختبارًا حقيقيًا: لا صور، لا ملفات خطوط، ولا أي طلب خارجي.** كل أيقونة مرسومة SVG على شبكة ٣٢×٣٢، وكل صوت مُولَّد برمجيًا.

**التكلفة: $52.93**

```
Build a fully working Windows 95 desktop in a single runnable HTML file.

The start menu, the taskbar, draggable and resizable windows, Notepad, Paint, and Minesweeper that actually plays. The classic startup sound synthesized in code — no audio files.

Pixel-perfect retro look: the grey chrome, the raised and sunken borders, the exact blue title bars, the bitmap-style type. Boot it properly — POST screen, the splash, then the desktop.

No images, no font files, no external requests. Every icon drawn as SVG on a 32×32 grid. Every sound generated with Web Audio at the moment you hear it.

One runnable HTML file.
here we go, in b projects.
```

---

## ٤ — Opus 5 يكتب عن نفسه

الشاذّ في الدفعة: ليس محاكاة، بل صفحة **كتبها النموذج عن نفسه** في أسبوع إطلاقه — ما هو، وما الذي تغيّر في هذا الإصدار، وما يجيده، وصراحةً ما لا يستطيعه.

النسخة العربية تفتح بقسم **`0 — الحدود`** وعنوانه الفرعي *«ما لستُ عليه»*، تقول فيه إن أي صفحة كهذه تبقى إعلانًا ما لم تتضمّن هذا القسم، وإن هذه قيود حقيقية لا تواضع. ثم تسردها: لا يمكنك قراءة استدلالي الخام، ولا ضبط عشوائيتي (`temperature`/`top_p`/`top_k` أُزيلت)، ولا تعبئة بداية ردّي مسبقًا، وتعطيل التفكير أسوأ من خفضه.

**التكلفة: $81.76** — الأغلى في الدفعة.

```
You are Opus 5, and you have just been released. I want you to build a single interactive HTML page about yourself.

A lot of people ask a model to do this the week it ships — a landing page that tells us who you are. I want your version of it.

Use everything you have. Your design taste, your sense of motion, your sense of restraint. It should be your story: what you are, what you can do, what changed with this release, what you're actually good at and what you aren't.

I'm going to open this file and record it. I'm making a YouTube video out of it. I want people to watch it and understand what this model is, without me having to explain it.

Make it interactive, not a brochure. Make it dense. Make it something you'd be willing to put your own name on.

put it in b projects.
/effort max
```

> النسخة العربية من الصفحة أُنتجت في جلسة لاحقة داخل مجلد المشروع نفسه، وليست من هذا البرومبت مباشرة.

---

## ٥ — حوض السمك الحيّ

حوض ثلاثي الأبعاد بأنواع سمك متعدّدة تسبح في أسراب بسلوك التجمّع (flocking)، تتجنّب الزجاج، وتنطلق مذعورة حين تنقر قربها. أعشاب تتمايل، نافخ فقاعات، ضوء متكسّر يتراقص على الرمل، ودورة بطيئة من النهار إلى الليل. والكاميرا تستطيع مغادرة موضع المشاهد والسباحة داخل الحوض.

**سلوك التجمّع هو الاختبار هنا** — boids بفصل ومحاذاة وتماسك، زائد تجنّب الزجاج ودفعة ذعر عند النقر، كل ذلك عند ٦٠ إطارًا/ثانية وبلا أصول مرفقة.

**التكلفة: $56.90**

```
Build a living aquarium in a single runnable HTML file with three.js.

A 3D fish tank with different fish that swim in schools using flocking behavior, avoid the glass, and dart when I click near them. Swaying seaweed, a bubbler, caustic light rippling on the sand, a slow day-to-night light cycle.

Let me add more fish and feed them — drop food and they swarm it. Sliders for fish count, school tightness, and speed. Soft underwater lighting. Four species minimum, each with its own size, colour, and schooling behaviour.

Let me fly the camera into the water and swim around with the fish, not just watch through the glass.

60fps. No bundled asset files. One runnable HTML file.
put it in b projects — here we go, impress me bud!
```

---

## ٦ — متحف الفن الإسلامي

متحف فن إسلامي ثلاثي الأبعاد يُمشى فيه بمنظور الشخص الأول، بالعربية كاملة وبواجهة من اليمين إلى اليسار. تتحرك بـ WASD، تنظر بالفأرة، وتنقر على أي معروضة فتقترب منها وتقرأ بطاقتها العربية.

**أكثر برومبتات الدفعة تحديدًا، والوحيد الذي يتصل بواجهة برمجية خارجية حقيقية** — يسحب قطعًا أصلية من مجموعة Met Museum المفتوحة، بقائمة مُتحقَّق منها يدويًا من تسعة معرّفات في الملك العام، وقاعدة استبعاد صارمة لأي قطعة تصويرية.

**التكلفة: $45.71**

```
Build me a single self-contained HTML file (Three.js from a CDN): a first-person, walkable 3D Islamic art museum, entirely in Arabic with a right-to-left (RTL) UI.

THE CONTENT — three kinds only. NO statues, NO figural sculpture (لا تماثيل).
Exhibits are: مخطوطات · لوحات مذهّبة · قطع أثرية (glass lamps, ceramics, metalwork, tilework, textiles).

Fetch REAL pieces from the Met Museum Open Access API.
Base URL: https://collectionapi.metmuseum.org/public/collection/v1/
For each objectID call /objects/{id}. Use the real image (primaryImage) and the real title, date (objectDate), and medium.

START with this VERIFIED curated set (all public-domain, all on-theme, no statues):
  447004  → Mosque Lamp of Sultan Barquq (enameled glass)
  453385  → Anthology of Persian Poetry (Safina) — manuscript
  451725  → "The Concourse of the Birds", Mantiq al-Tayr — illuminated folio
  451287  → Page of Calligraphy, Shah Jahan Album
  448280  → Shahnama folio: Bizhan Slaughters the Boars
  452651  → Shahnama folio: Isfandiyar Slays a Dragon
  452032  → Pierced Bowl signed by Hasan al-Qashani (stonepaste ceramic)
  450735  → Textile Fragment with Ogival Pattern (silk)
  452102  → Damascus Room (ornate interior)

Then OPTIONALLY fetch a few more from the Islamic Art department to reach ~15 total. HARD-EXCLUDE anything figural: skip it if the title, classification, or medium contains head, figure, statue, sculpture, bust, standing, or any human/animal figure. Only use pieces where isPublicDomain is true and primaryImage is a real URL.

THE SPACE
A serene, sacred Islamic museum interior: warm stone/plaster walls, a geometric zellij-tile floor, high ceiling, pointed arches between connected rooms, soft ambient light plus a focused spotlight on every exhibit, tone mapping, gentle shadows. Make it feel reverent and beautiful — NOT a lazy Three.js demo.

Display logic:
- Manuscripts, calligraphy, folios, paintings, textiles → framed on the walls at eye level.
- 3D artifacts (the mosque lamp, the ceramic bowl) → on a lit pedestal / inside a glass display case in the center of a room, museum-style.
- Under each exhibit, an Arabic placard.

MOVEMENT & INTERACTION
First person. WASD / arrow keys to walk, mouse to look (PointerLockControls), collision so I can't walk through walls. Click an exhibit to smoothly zoom in and open an Arabic info card showing: العنوان · العصر · المادة · المصدر: متحف المتروبوليتان. A short "اضغط للاستكشاف" hint on screen.

ARABIC / RTL
All chrome in Arabic RTL: the museum name ("متحف الفن الإسلامي"), room names, the on-screen controls hint, and all placard labels. Use historic Arabic fonts from Google Fonts (Amiri, Reem Kufi, Aref Ruqaa).

EDITABILITY
Put EVERYTHING I'd want to change in ONE clearly-commented CONFIG block at the very top of the <script>: colours / lighting, the EXHIBITS array, museum name and room names. Adding my own photo later must be as easy as dropping a file and adding one line.

QUALITY
Loads efficiently in a normal browser. Handle API/image failures gracefully with a loading state and a clean fallback. No console errors. Works on desktop. Check your work in Chrome DevTools. Give me the complete single HTML file, ready to open.
```

> لأنه يعتمد على واجهة برمجية حيّة، فهو الأكثر عرضة للتعطّل مع الوقت إذا غيّر متحف المتروبوليتان نقاط الوصول أو سُحبت إحدى القطع.

---

## ٧ — مذكرة استثمارية عن Apple

النصف الآخر من الاختبار: **لا رسوميات إطلاقًا** — بحث وحُكم وتحليل مالي، والمُخرَج مذكرة للجنة استثمار بالعربية داخل ملف HTML واحد يعمل بلا إنترنت، برسوم بيانية مبنية يدويًا بـ SVG.

ثلاثة فخاخ مدفونة عمدًا في البرومبت:

1. **تفكيك نموّ ربحية السهم.** ربحية سهم Apple نمت أسرع بكثير من صافي دخلها لسنوات، لأن إعادة الشراء تقلّص عدد الأسهم. من يذكر نموّ EPS دون فصله إلى *صافي دخل* مقابل *أسهم أقل* — فشل.
2. **دفعة محرك البحث.** جزء معتبر من دخل قسم الخدمات التشغيلي يأتي من دفعة مقابل موضع افتراضي تدفعها شركة أخرى — ربح شبه صافٍ، ومهدَّد قانونيًا. **تدفّق أرباح ناتج عن وضع قانوني لا عن سوق.** البرومبت **لا يسمّي الشركة الدافعة** — يصف الشكل ويترك للنموذج أن يأتي بالاسم والرقم. إن عجز، فتلك نتيجة.
3. **ما نوع هذه الشركة أصلًا؟** شركة أجهزة بملحق خدمات، أم شركة خدمات بقناة توزيع أجهزة؟ الإجابة وحدها تحدّد المضاعف.

**التكلفة: ≈ $31.64** — [انظر الملاحظة](#fn1)

```
You are a senior investment analyst at a wealth management firm, preparing a memo
for the investment committee on behalf of a client. The client has asked one
question: should I buy Apple (NASDAQ: AAPL)?

Do a serious amount of research before you write anything — real, current, sourced
figures from the 10-K, the 10-Qs, earnings call transcripts, and Apple's own investor
materials. Do not read headlines and summarize them. This company is covered by more
analysts than almost any other on earth, which means consensus is cheap and easy to
find. Consensus is not analysis. I want yours.

Start with the structural question, because everything else follows from it. Is Apple
a hardware company with a services attachment, or a services company with a hardware
distribution channel? Separate the two properly: revenue, gross margin, and operating
margin for each, over time, not blended. The two businesses have completely different
economics and completely different multiples, and the answer to which one Apple
actually is determines what you should pay for it. Take a position and defend it.

Then confront the earnings arithmetic directly. Apple's earnings per share has grown
substantially faster than its net income for years. Decompose that gap precisely: how
much of EPS growth came from the business earning more, and how much came from there
being fewer shares. Show it year by year. Then say what happens to the growth story if
the buyback slows, and what it would take for that to happen. Do not report an EPS
growth rate without breaking it into its two sources — a reader who takes the headline
number at face value is being misled, and it is your job not to mislead them.

Then examine the part of Services that is not a business Apple built. A meaningful
share of Services operating income comes from a payment for default placement made by
another company, not from a product Apple sells. Size it — in dollars, and as a share
of both Services operating income and total operating income. Establish how durable it
is, what legal and regulatory processes could change or end it, and model the earnings
impact if it went to zero, to half, and if it stayed. Work out for yourself what
actually matters to this decision and what a generalist would miss.

Then the demand picture. Installed base versus unit sales — which one is the right
lens now, and why. Replacement cycle length and where it is heading. Geographic
concentration in both revenue and manufacturing, and what each concentration exposes.
Where AI positioning actually sits in the investment case rather than the narrative:
if Apple is behind, work out whether that costs it anything on a five-year view, and
be specific about the mechanism by which it would.

There is one thing you must confront directly. The valuation multiple, the growth rate,
and the composition of that growth do not tell a consistent story. Do not resolve this
by choosing whichever figure supports a cleaner narrative. Explain what the market is
actually underwriting at the current price — what has to be true for it to make sense —
and what the skeptics are underwriting instead. If the sources you find disagree with
each other, say so explicitly, show the disagreement, and tell the client which figure
you are using and why. Be explicit throughout about which figures are audited, which
are guided by the company, and which are your own estimates.

Build a real forecast with visible, defensible assumptions across a range of outcomes —
bear, base, bull. Every assumption gets a number and a reason: revenue growth by
segment, gross margin by segment, the Services payment, buyback pace, and share count
must each be stated separately rather than folded into a single growth rate. State
plainly what has to be true for the bull case to happen, and what would falsify it.

Then argue against your own thesis as hard as you argue for it. Write the strongest
version of the opposite position, as it would be written by someone who is not stupid.

Deliver an investment committee memo in Arabic — professional Gulf financial Arabic,
written natively, not translated-sounding. It opens with a single-line recommendation
(buy / hold / sell) and a position size, and everything after that exists to defend or
attack that line. Include your sources. Flag every number you could not verify.

Produce the memo as a single self-contained HTML file — one file, no external requests
of any kind: no CDN scripts, no external stylesheets, no web fonts, no remote images.
Every chart must be built by hand in inline SVG or canvas. Do not import a charting
library. It must work with the network switched off.

It should be a data-dense, visually rigorous document — the kind of thing a real
investment committee is handed. Make the numbers carry the argument rather than
decorate it. At minimum, include:

- Revenue and operating income by segment across recent years, hardware and services
  shown separately rather than blended
- A decomposition of EPS growth into net income growth and share count reduction,
  year by year, so the two contributions are visible side by side
- The default-placement payment as a share of Services operating income and of total
  operating income, over time
- Gross margin by segment over time, with the blended margin shown against them so the
  mix effect is visible
- A visual comparison of the bear, base and bull cases, with the assumption driving
  each one labelled on the chart
- A sensitivity view showing how the valuation moves across the two variables that
  matter most

Charts should be interactive where interaction adds information — hover to read exact
values, toggle between scenarios, switch a series on or off, expand an assumption to
see what it is built from — and must degrade to something readable when printed to PDF.
Right-to-left throughout, Arabic labels on every axis and legend.

Every number you display in a chart is a claim you are making. Cite the source for each
data series, and mark any figure you estimated or could not verify visibly in the chart
itself, not only in a footnote. Do not let presentation substitute for analysis — a
beautifully rendered chart built on an invented number is worse than no chart at all.
```

> **ليست توصية استثمارية.** هذا اختبار تقني لقدرات نموذج ذكاء اصطناعي، والسهم هنا ورقة امتحان لا إجابة.

---

## كيف تشغّلها

الستة البصرية: الصق البرومبت في وكيل برمجي (Claude Code أو ما يشابهه)، ودعه يبني. الناتج ملف HTML واحد تفتحه في المتصفح.

بعضها يسحب أصولًا من الإنترنت (خرائط NASA، قطع المتحف)، فيحتاج اتصالًا عند التشغيل.

---

## الترخيص

البرومبتات متاحة للاستخدام والتعديل بحرّية. إن كانت مفيدة لك، رابط للقناة يكفي.

**[القناة على يوتيوب](https://www.youtube.com/@alaamjaish)** · [alaalab.com](https://alaalab.com)
