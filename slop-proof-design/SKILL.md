---
name: slop-proof-design
description: Anti-slop for design. A sourced list of what to avoid in web pages and UI, social graphics and ads, slides, charts, logos, icons and AI images and video. Use it as guardrails before designing or as a review pass that lists hits by id. It never designs or sets a style.
---

# Slop-proof design

A list of things to avoid. It does not design or set a style: the brief, the brand and the owner's taste decide the look. Each item says what the problem looks like, why it hurts or reads as AI-made, and how to spot it. [n] points to SOURCES.md.

## How to use it

**Tags.** Each item has one:
- **Floor**: accessibility, legibility or honesty. Always a hit.
- **Rule**: a sourced usability or craft failure. A hit unless the brief breaks it on purpose.
- **Tell**: a default that reads as AI-made. One alone is fine if the brief chose it. Several together read as generated; one practitioner puts the threshold at 6 to 8 [1].

**While designing.** Load this as guardrails. Nothing here says what to make instead.

**When reviewing.**
1. Look at the real thing. Render web and UI at 1280px and 375px wide. View images at 100% and as a thumbnail, slides at presentation size, ads at feed size. Measure the rendered result, not the code or the prompt.
2. Scan only the areas that apply, plus X (all media).
3. List each hit as `id: where: what`, for example `C1: .sub on hero: 3.2:1`.
4. Propose the smallest fix for each hit, floors first. Don't redesign, swap one default for another (X7) or strip real content, including footers and legal lines.
5. Invent nothing: no new facts, numbers, customers, quotes or filler lines. Mark a missing real item with a slot such as [product photo].
6. Report hits, fixes, and anything left alone on purpose, with the reason.

**New** marks avoids backed mainly by sources from May to October 2026: current image and video models, vibe-coding site builders and AI slide tools. Ids are stable; a removed item leaves a gap.

## X. Content and honesty (all media)

**X1. Avoid invented facts.** Floor. Numbers, customers, quotes, features or data not in the brief or original, even in mock-ups. Why: AI-made decks and pages carry unsourced numbers and fabricated facts [2][3][4]; US ads that claim to show "actual consumers" must use real ones [5]. Spot: trace every claim to a source the owner supplied.

**X2. Avoid fake proof furniture.** Tell (Floor if invented). Round-number stat banners, star ratings, "Trusted by" logo bars and placeholder testimonials [6][7]. Spot: proof with no name, date or source attached.

**X3. Avoid synthetic people, places or products where trust matters.** Floor. AI-made people or settings in health, finance, travel or big purchases [8][9]. Why: 62% of Americans reject AI-made people in ads even when disclosed [10]; disclosed AI luxury ads are seen as lower effort and less authentic [11]; the EU requires deepfake labels from 2 August 2026 [12]. Spot: a generated person or place shown as real [13][14].

**X4. Avoid a design that could belong to anyone.** Tell. Swap in a competitor's logo and nothing else would need to change [15][16][17]. Spot: no detail only this subject has.

**X5. Avoid shipping the first output.** Tell. One generation with no critique pass [18]. Why: the only AI ad NIQ's viewers did not pick as AI was heavily edited by professionals [19]. Spot: flaws one look at full size would catch.

**X6. Avoid leftovers.** Floor. "Made with [tool]" watermarks, an "Edit with Lovable" tab or "Built with v0" footer line [20], lorem ipsum, prompt text and process notes left in the design [4]. Spot: read every word, including small print and image corners.

**X7. Avoid swapping one default for another.** Tell. Dodging one stock look into the next: purple gradients into cream, serif and terracotta, or near-black with acid green [21][22]. Told to avoid Inter, one model moved straight to Space Grotesk [15]. A bare text page is the same mistake. Spot: a fix that matches another item on this list.

**X8. Avoid the untouched builder kit.** Tell, New. shadcn/ui components with the default grey palette, Lucide icons on every card, Inter or Geist, pill buttons, rounded corners on everything, often on a dark page with a purple-to-blue headline [20][23]. Builders such as Lovable, Bolt and v0 share this stack, so their output converges on one look [20]. Spot: nothing in the theme was changed from the library default.

## L. Layout and spacing

**L1. Avoid spacing off a scale.** Rule, New. Gaps like 13, 18, 22, 30 and 44px with no pattern, or 24, 28 and 32px used for the same job [1][24]. Why: a short scale on a base unit keeps rhythm (Material uses 8dp [25]), with steps at least 25% apart [26]. Spot: list the computed margins and gaps.

**L2. Avoid groups that do not group.** Rule. The same space inside a group as between groups; a heading as close to the section above as to its own content [27][28]. Spot: blur the view; groups should still read as groups.

**L3. Avoid ragged edges.** Rule. Text, icons and images starting on many different left edges, blocks that ignore the column grid [25][29]. Spot: count distinct left edges.

**L4. Avoid competing focal points.** Rule. No one most important thing, more than two large elements fighting for first look [28], or a big moving visual that drowns the headline [30]. Why: making everything loud makes nothing loud; mute competitors instead [26]. Spot: the squint test shows no single first stop [28].

**L5. Avoid stretching content to fill the screen.** Rule. Text and cards spread across the full width because the space is there [26].

**L6. Avoid a reading order that differs from the visual order.** Floor. Source or tab order that jumps around what the eye sees [31]. Spot: tab through, or read the DOM order.

**L7. Avoid a first screen that misses the point.** Rule (web). The offer and main action below the fold, or a hero sized for one screen that misses others [32]. Why: about 57% of page viewing time is above the fold [33]. Spot: at 1280 and 375px, can you say what it is and what to do without scrolling?

**L8. Avoid the template hero.** Tell. Centred pill badge, big headline, one-line subhead, one or two buttons, over a gradient [6][34][7].

**L9. Avoid three identical cards.** Tell. Three equal cards, each with an icon, a two-word title and one line [6][34][18].

**L10. Avoid the section kit.** Tell. Stat banner, 1-2-3 steps, FAQ accordion, logo bar, three pricing tiers with "Most Popular", a four-column footer [6][7], an email sign-up closing every page [32], there because templates have them. Spot: sections with thin content.

**L11. Avoid a card around everything.** Tell, New. Boxes inside boxes, each with its own border, fill or shadow; every block wrapped in a card [35]. Spot: more than one container level for one group.

**L12. Avoid a bento grid by default.** Tell. A mosaic of mixed-size rounded tiles for content with no such shape [22][36].

**L13. Avoid hero clutter.** Tell. Floating badges, chips, stickers or mini-cards scattered over the hero [17].

**L14. Avoid decoration in place of the subject.** Tell. Glowing orbs, blobs, iridescent 3D shapes and dot grids where the product should be [34][7]. Spot: remove it; if nothing is lost, it was filler.

## Y. Type

**Y1. Avoid web body text under 16px.** Rule. Small grey body copy. Why: web body text reads well at 15 to 25px [37][38]; under 16px sits at the bottom edge. Spot: computed paragraph size at both widths.

**Y2. Avoid lines too long or too short.** Rule. Body lines outside 45 to 75 characters [39][40]; over 80 fails WCAG AAA [41]. Spot: count characters in a typical line at 1280px.

**Y3. Avoid cramped or clipping text.** Floor. Body line spacing outside about 120% to 145% [37][38]; text boxes with a fixed height. Why: text must not clip when users set line height 1.5, paragraph spacing 2, letter spacing 0.12 and word spacing 0.16 times the font size [42]. Spot: apply those overrides and look for overlap.

**Y4. Avoid too many sizes and levels.** Rule. More than three text sizes or three contrast levels in a view [28][43]; a new type size in every section, or every section heading at the same weight [24]. Sizes picked ad hoc, not from a short list [26]. Spot: list the computed sizes.

**Y5. Avoid three or more typefaces.** Rule. Most designs carry a second typeface; few carry a third [44]. Three fonts is a listed AI tell [24]. Spot: count families.

**Y6. Avoid thin or many weights.** Rule. Interface text under weight 400, or more than two weights doing one job [45].

**Y7. Avoid caps paragraphs and badly spaced caps.** Rule. Caps beyond a short label read about 13% slower [46]; caps need 5% to 12% extra letter spacing, lowercase body text none [37]. Spot: caps runs longer than one line.

**Y8. Avoid justified text without hyphenation.** Rule. Both edges straight, with rivers of space between words [38][41].

**Y9. Avoid straight quotes and wobbling figures.** Rule. Straight quotes in display text [37]; proportional figures in tables or numbers people compare [38]. Spot: columns of numbers that do not line up.

**Y10. Avoid default fonts and the accent word.** Tell. Inter, Roboto or a system font for everything [15][6][16][7]; Space Grotesk, Instrument Serif or Geist as the trendy pairing; one italic serif or coloured word in the headline [15][21][6][1][32]; italics in headers [47].

**Y11. Avoid eyebrow labels and fake numbering.** Tell, New. Small tracked caps or a small monospace pre-heading above every heading ("FEATURES"), called "the mdash of UI design" in October 2026 [48][32]; all-caps pills with wide letter spacing [47]; 01, 02, 03 on items with no order [21][6][36][24]. Spot: a label that repeats the heading under it.

**Y12. Avoid punctuation chrome.** Tell, New. Meta strings joined by middle dots, an arrow on every link [21][24], em dashes in interface copy [1][3].

## C. Colour and contrast

**C1. Avoid text under contrast floors.** Floor. Text under 4.5:1, or large text (24px, or 18.5px bold) under 3:1 [49]. Low-contrast text is the most common accessibility failure, on 83.9% of top home pages in 2026 [50]. Spot: measure every text pair; 4.49:1 fails.

**C2. Avoid faint controls and marks.** Floor. Input borders, icons, focus rings and chart marks under 3:1 against what is next to them [51]. Inactive controls are exempt; a control with a passing label needs no 3:1 border [51].

**C3. Avoid text over busy or variable backgrounds.** Floor. Text over a photo, gradient or translucent panel that drops under 4.5:1 anywhere [49]. Why: on glass, contrast varies across one line [52]; in iOS 26, translucency over busy content hides text and controls [53]. Spot: measure the worst pixels, not the average.

**C4. Avoid meaning by colour alone.** Floor. Status, errors, links or chart series told apart only by colour [28][54]. Why: about 8% of men of European descent have red-green colour deficiency [55]; red against green fails them [56][57]. Spot: view in greyscale.

**C5. Avoid grey or faded text on colour.** Rule. Secondary text on a coloured background set in grey or lowered opacity [45][58]. Spot: grey text on a tinted panel; then re-check C1.

**C6. Avoid fully saturated accents on dark surfaces.** Rule. Material's dark theme desaturates colours for dark surfaces [59]. Spot: pure hues on near-black.

**C7. Avoid treating APCA or WCAG 3 scores as a pass.** Rule. WCAG 3 is still a draft [60]; APCA is advice, not conformance [61]. Spot: a report citing Lc values with no WCAG 2 ratio.

**C8. Avoid the purple-blue gradient.** Tell. Violet-to-indigo washes on the hero or buttons, often with gradient headline text [15][6][34][7]. Spot: colour with no link to the subject [18].

**C9. Avoid dark mode with grey text.** Tell. Near-black background with mid-grey body text that barely passes [21][6]; pure #000 surfaces with no light mode [62]. Spot: body text near the 4.5:1 line on dark.

## M. Motion and effects

**M1. Avoid motion people cannot stop.** Floor. Carousels, marquees or animations that move for more than 5 seconds without a way to pause, stop or hide them [63]. Why: auto-forwarding carousels move content away before people read it [64][65]. Spot: anything still moving after 5 seconds.

**M2. Avoid ignoring reduced motion.** Floor. Parallax, zooms and large movement on scroll or click with no off switch; `prefers-reduced-motion` ignored [66][7]. Why: it can make people with vestibular disorders ill [66]. Spot: turn on reduced motion and reload.

**M3. Avoid motion on everything.** Tell, New. Every section fades up, every card lifts on hover [21][18][7]. Content hidden until a scroll animation fires, so a slow or blocked script leaves a blank page [1]. Spot: disable scripts or scroll fast.

**M4. Avoid gimmick texture and motion.** Tell, New. Grid-paper or grain backgrounds, logo marquees, bouncing buttons, blinking cursors, pulsing dots travelling along connector lines, a glow that follows the cursor, confetti [36][22][1]. Spot: motion that reports nothing real.

**M5. Avoid glassmorphism by default.** Tell. Translucent blurred panels over a gradient [6][34][7], used as style rather than for real overlays. Why: it adds contrast failures (C3) [52][53]. Spot: frosted panels on a static page.

**M6. Avoid one shadow and radius on everything, or a mix with no logic.** Tell. The same soft shadow and large radius (20px or more) everywhere [21][18][7][62], or radii of 8, 12, 16 and 24px and shadows on some cards but not others [24]. Spot: list radius and shadow values by element role.

**M7. Avoid accent stripes.** Tell. A coloured top or left border on each card [6][36]. Spot: stripes that mean nothing.

**M8. Avoid glows, sparkles and shimmer.** Tell. Big coloured glows, sparkles for anything AI [67], shimmer on things that are not loading [6][7]. Spot: emphasis that does not come from size, weight, position or contrast [45].

## U. Interface and interaction

**U1. Avoid hidden focus.** Floor. Focus outlines removed, or too faint to see [68][35]. Custom focus rings under 2px or under a 3:1 change [69]. Spot: tab through every control.

**U2. Avoid small targets.** Floor. Controls under 24 by 24 CSS px without enough spacing [70]; under 44 by 44pt on Apple platforms [71]. Spot: measure the rendered box, not the padding value.

**U3. Avoid placeholders as labels.** Floor. Fields labelled only by placeholder text, or not at all. Why: the hint vanishes on typing, strains memory and is usually low contrast [72]; missing labels are on 51% of top home pages [50]. Spot: type into each field.

**U4. Avoid controls with no name.** Floor. Icon-only buttons and links with no accessible text; empty buttons on 30.6% and empty links on 46.3% of top home pages [50]. Spot: read the accessible name of every control.

**U5. Avoid weak signifiers.** Rule. Links styled as plain text, ghost buttons as the main action, flat elements that do not look clickable. Why: weak signifiers cost 22% more time and 25% more fixations in NN/g testing [73]. Spot: can you tell what is clickable from a screenshot?

**U6. Avoid hiding the main navigation on desktop.** Rule. A hamburger menu where there is room for visible links. Why: hiding navigation cut discoverability almost in half and raised task time and difficulty [74]. Spot: a hamburger at 1280px.

**U7. Avoid carousels for key content.** Rule. The main message in slide 2 of 5. Why: people miss rotating content [64][65].

**U8. Avoid several primary actions.** Rule. More than one solid primary button per view [45], or two hero buttons of equal weight [30]. Spot: count filled buttons in each view.

**U9. Avoid inconsistent roles and broken conventions.** Rule. One role (button, link, card, heading level) styled several ways, or controls that work against platform habits [75]. Why: genre-familiar layouts are judged more appealing within 50ms [76][77].

**U10. Avoid missing and fake states.** Floor, New. Only the happy path exists: no loading, empty or error states [35]; a form that says thanks without sending anything [32]. Spot: load with no data, a slow network and a failing request.

**U11. Avoid layouts that break when narrow or zoomed.** Floor. Two-way scrolling, clipped or overlapping content at 320 CSS px wide or 400% zoom [78]. Spot: set the viewport to 320px.

**U12. Avoid stock controls and lazy hover.** Tell, New. Library-default buttons and inputs, hover states that only fade opacity [1].

**U13. Avoid placeholder icons and emoji bullets.** Tell. The obvious icon in a tinted rounded square; rockets and bolts as bullets [6][34][7]; thin icons that only roughly match their label [1]; emoji as interface icons [23][47]. Spot: cover the label; does the icon still say it?

## W. Words on the design

**W1. Avoid burying the key words.** Rule. Headings and list items that open with filler. Why: people scan the top lines and left edge [79], often only the first two words [80]; 80% of fixations fall on the left half of a page [81]; layered headings let a page be scanned [82]. Spot: read only the first two words of each heading.

**W2. Avoid vague link text.** Floor. "Click here", "more", "learn more" with nothing around them to say where they go [83]; on 15.2% of top home pages [50]. Spot: read the links alone, out of context.

**W3. Avoid lines that could sell anything.** Tell. "Revolutionize your workflow", "Unlock your potential", reassuring lines with no fact ("Built for how you work") [18][7]. Spot: a line that fits a competitor word for word.

**W4. Avoid AI vocabulary.** Tell. Seamless, elevate, supercharge, game-changing, cutting-edge, delve, vibrant [18][84][7]. Spot: search for them.

**W5. Avoid stock sentence shapes.** Tell. "Not just X, it's Y", "not only A, but also B", and triplets like "fast, simple and secure" [84][3]. Spot: lists of three everywhere.

**W6. Avoid default buttons and casing.** Tell. "Get started" on every button [7]; a "Scroll to explore" cue [47]; Title Case On Every Heading [84]. Spot: a button that does not say what happens next.

## P. Photos, AI images and video

**P1. Avoid generated text in images.** Floor. Gibberish signage, misshapen letters, a wrong letter in a logo [85][86]. Why: text-to-image models still produce typos and missing or extra characters [87]; in a September 2026 test of the newest models, a dense street scene still had a spelling slip and a sticker that garbled its own text [88]. Spot: read every letter at 100%.

**P2. Avoid broken anatomy.** Floor. Extra or fused fingers, odd teeth, limbs that bend wrong, glasses merging into faces [89][90][85][91][86]. Why: in a 340,000-image study, abnormal human anatomy made up 61.5% of flawed images and hand deformity 31.9% [92]. Spot: zoom on hands, eyes, teeth and joints.

**P3. Avoid objects that merge or could not work.** Floor. Objects passing through each other, straps melting into hands, meaningless dials, a product that changes shape [89][93]. Abnormal overlap between elements was in 27% of flawed images [92]. Spot: trace every edge where two things meet.

**P4. Avoid generated group shots without a close check.** Rule. Scenes with several people score far worse than single-subject ones [92]. Spot: check every person, not just the front one.

**P5. Avoid light, shadow and perspective that disagree.** Rule. Shadows falling different ways, warped perspective, reflections that do not match [89][90][91][86]. Spot: check every shadow against the light source.

**P6. Avoid too-perfect faces.** Tell. Poreless, shiny, too-gorgeous faces [90][91]. AI faces are more average and attractive than real ones [94], and people spot them at chance, 48.2% [95]. Spot: irregular pupils and mismatched catchlights [96][97].

**P7. Avoid the glossy AI look.** Tell. Oversaturated colour, exaggerated rim light, cinematic backgrounds, generic bokeh, overperfection [90][91][98]. A grain filter does not hide it [99]. Spot: the image could be from any brand's feed.

**P8. Avoid generic aspirational scenes.** Tell. A figure gazing into the distance, staged teamwork, scenes that could sell anything [98][100]. Spot: nothing in the frame is specific to this subject.

**P9. Avoid decorative images where the real thing exists.** Rule. Stock or generated filler instead of the actual product, place or team. Why: users study real product and people photos and ignore decorative and stock images [101].

**P10. Avoid mismatched image sets.** Rule. One set with mixed sizes, ratios, crops or treatments [25]. Spot: line up the set side by side.

**P11. Avoid style and object drift across a set.** Tell. A series or video that switches between realism and a cartoon look, or a product that differs in every shot [102][103]. Viewers of one AI holiday ad cited realism, execution and fit in their backlash [104]. Spot: compare the same object across frames.

**P12. Avoid the AI illustration look.** Tell. Faux-sketch or soft rendering over a generic pretty face; folds and perspective that break the style's own rules [99][105]. Spot: the style holds only at thumbnail size.

**P13. Avoid trusting old tells either way.** Rule, New. In current video, floating hands, flickering light and distorted faces are largely gone [106]; Nano Banana models left the glossy portrait look behind [107]. A clean image is not cleared, and a missing watermark proves nothing [108]. One odd detail is not proof either; detectors miss and mislabel [89][86], and one study found detection at about 76% [93]. Spot: check text, counts, edges and facts; need two kinds of error before calling it.

**P14. Avoid images with no text alternative.** Floor. Informative images with no alt text; missing alt text is on 53.1% of top home pages [50]. Spot: read the alt attribute of every meaningful image.

**P15. Avoid generated video that drifts.** Floor, New. Objects or faces that change shape between frames, sign or shirt text that reorganises, cloth and liquid that move without weight, background people who repeat or melt, audio out of sync [108][106]; one smooth cinematic shot with no cut [108]. Spot: step through frame by frame and compare.

**P16. Avoid generated infographics and text-heavy slides as images.** Floor, New. Charts, infographics or slides made as one image, with facts and words baked in. Why: in recent tests a research infographic came back with a wrong year [88], and Nano Banana 2's infographics and charts showed more hallucinations and a house style of one font with the same borders, shadows and icons every time [109]. Spot: check every number, date and word against the source.

## D. Charts

**D1. Avoid a chart type that hides the comparison.** Rule. Angle, area or shading where amounts are compared. Why: position on a shared scale reads most accurately, then length, then angle and area, shading worst [110][111]; bars or dots suit amounts, lines suit change over time [112]. Spot: is the key comparison on a shared axis?

**D2. Avoid truncated bar axes.** Floor. Bars that do not start at zero, so small gaps look large [113][114]. Line charts may zoom when change is the point [113]; a zero baseline is not always right for them [115]. Spot: read the bar axis minimum.

**D3. Avoid 3D, dual axes and crowded pies.** Rule. Depth makes values slower and harder to read [116]; two y-axes let scales invent a relationship [117]; pies with many or exploded slices [118]. Spot: any perspective, second axis or pie over a few slices.

**D4. Avoid colour scales that misread the data.** Rule. Rainbow scales [119]; more than 8 categorical colours, where 3 to 5 is comfortable [120][121]; continuous numbers mapped to hues, which exaggerates differences [115]; diverging scales with no real midpoint [121]. Spot: does each colour step mean a data step?

**D5. Avoid reversed conventions.** Rule. Up or darker meaning less [115]. Spot: does the largest value sit highest and darkest?

**D6. Avoid legends where labels fit.** Rule. A legend forces back-and-forth and taxes working memory [115][122]. Spot: a legend for series that could be labelled directly.

**D7. Avoid titles that name the topic.** Rule. "Revenue by region" instead of the finding. Why: people recall titles and annotations that carry the message [123][124]. Spot: does the title say what the chart shows?

**D8. Avoid unsorted bars and heavy gridlines.** Rule. Bars in arbitrary order; dark grids that compete with the data [122][114]. Spot: bars with no logic to their order.

**D9. Avoid chart decoration.** Tell. Gradient or glowing bars, shadows on marks, a legend repeating the axis [119][113][122]. Spot: ink that encodes nothing.

**D10. Avoid unchecked generated chart values.** Floor. LLM-made charts were less accurate than human-made ones in testing [125]. Spot: check every plotted value against the source data.

**D11. Avoid distracting chart animation.** Rule. Bars that bounce in or series that move while people read [115]. Spot: motion that does not show a change in the data.

## S. Slides

**S1. Avoid topic labels and bullet walls.** Rule. Headlines like "Results" over bullets, where the point should be. Why: sentence headlines backed by a visual raised recall from 69% to 79% [126][127]. Spot: do the headlines alone carry the argument?

**S2. Avoid type too small for the room.** Floor. Headlines under 28pt, body under 18pt, callouts under 14pt [127]. Spot: check sizes at presentation scale.

**S3. Avoid the script on the slide.** Rule. Speaker notes pasted as slide text; labels set apart from what they name [128]. Spot: paragraphs on a slide.

**S4. Avoid deck sameness.** Tell, New. Every slide the same layout and visual weight: topic title, bullets, a generic image [129][4]; always three cards; everything centred [2]; every card the same medium-loud density [130]. Spot: view as thumbnails; can you tell the slides apart?

**S5. Avoid decoration with no job.** Tell, New. Abstract 3D spheres, glassy gradients [4][3], a single highlighted text box off to one side [3], shapes that hold nothing [2]. Spot: remove it; if nothing is lost, it was filler.

**S6. Avoid clipped text and spacing drift.** Floor, New. Text that overflows or is cut off because no one viewed the slide at full size; margins that shift from slide to slide [2]. Spot: page through at full size and watch the edges.

**S7. Avoid flattened hierarchy and ragged density.** Rule, New. Bullets of very different importance at the same weight; a sparse card spread thin next to a dense card crammed to the margins; emphasis by bold, colour and size on the same word at once; body text shrunk to fit [130]. Spot: one first stop per slide?

## G. Logos and icons

**G1. Avoid logos that fail small or in one colour.** Rule. Detail that vanishes at 16 and 32px [131]; no one-colour or reversed version; clear space not defined [132]; a favicon that is not square or is 48px or smaller [133]. Moderately detailed, natural marks are recognised best [134]. Spot: view at 16px in black only.

**G2. Avoid mixed icon families.** Rule. Icons with different grids, strokes, corners, sizes or perspective; weights that do not match nearby text; asymmetric icons not centred by eye [131][135]. Spot: line them up in a row.

**G3. Avoid unlabelled icons.** Rule. Few icons are understood without a word [136]; a sparkle does not reliably mean AI [67]. App icons with photos or thin strokes [137]. Spot: cover the labels and ask what each does.

**G4. Avoid the stock-glyph or orb logo.** Tell. A letter or stock icon in a gradient rounded square, a sparkle as the mark [131][67], the spherical or spiral orb many AI companies share [138], or a gradient logo [47]. Spot: the mark would suit any company in the category.

**G5. Avoid generated logos taken as finished.** Rule. In expert review, most logos from six AI logo makers lacked proportion, balance and unity [139]. Spot: check alignment, spacing and optical balance by hand.

**G6. Avoid uncleared generated marks.** Floor. AI logos may resemble existing trade marks; run a clearance search before use [140]. Spot: reverse image search and a trade mark search.

## A. Ads and social

**A1. Avoid more than one message.** Rule. Several offers or actions in one ad; copy past platform limits. Meta recommends primary text of about 125 characters and headlines of about 40 [141]; LinkedIn truncates intro text over 150 characters [142]. Spot: count characters and count asks.

**A2. Avoid a late or hidden brand.** Rule. Brand and product appearing late, or not in the brand's own colours and shapes [143][144]. Spot: is the brand visible in the first frame and at thumbnail size?

**A3. Avoid the wrong frame and covered zones.** Floor. A crop that misses the placement (4:5 feed, 9:16 Stories and Reels), or key text and logos under the platform's buttons and captions [145][146]. On a 1080 by 1920 YouTube Short, keep key content off the top 288px, bottom 672px, left 48px and right 192px [147]. Spot: overlay the platform's safe-zone guide.

**A4. Avoid generated visuals where effort is the message.** Rule. AI imagery in luxury, craft or holiday campaigns. Why: disclosed AI luxury ads were rated lower effort (3.81 against 5.28) and less authentic [11]; backlash to one AI holiday ad centred on realism, execution, authenticity and ethics [104][102]. Spot: would viewers feel a corner was cut?

## Final avoid-check

1. Honesty: invented facts, fake proof, leftovers, synthetic people where trust matters (X1 to X3, X6, U10)?
2. Contrast: text, controls or focus under floor, over images or glass; colour alone (C1 to C4, U1)?
3. Reading: body under 16px, lines outside 45 to 75 characters, clipping, too many sizes, weights or faces (Y1 to Y6)?
4. Access: small targets, unnamed controls, placeholder labels, vague links, no alt, breaks at 320px, order off (U2 to U4, U11, W2, P14, L6)?
5. Motion: can't be stopped, ignores reduced motion (M1, M2)?
6. Layout: off-scale spacing, weak groups, ragged edges, competing focal points (L1 to L4)?
7. Images and video: generated text, anatomy, merging objects, drift, baked-in infographics (P1 to P3, P11, P15, P16)?
8. Charts and slides: truncated bars, wrong type, misleading colour, unchecked values, small type, clipping, flat hierarchy (D1 to D5, D10, S1, S2, S6, S7)?
9. Logos and ads: fails at 16px or in one colour, uncleared, several messages, late brand, covered zones (G1, G6, A1 to A3)?
10. Tells: count X2, X4, X5, X7, X8, L8 to L14, Y10 to Y12, C8, C9, M3 to M8, U12, U13, W3 to W6, P6 to P8, P11, P12, D9, S4, S5, G4.
11. Fixes: did any add a fact, swap in another default or strip real content (X1, X7)?
