---
name: slop-proof-design
description: Use when making, editing or reviewing any visual design: web pages and UI, social graphics and ads, slides, charts, logos, icons and AI-generated images. Applies hard, sourced design rules and strips the default look of AI-made design.
---

# Slop-proof design

Make a design better in the style it already has: apply the hard rules, then remove the AI defaults.

Rule ids are stable; a removed rule leaves a gap. [n] points to SOURCES.md, where every number comes from.

## How to run it

1. Gather direction: the brief, the owner's approved work and brand rules, with concrete notes ("use this spacing", not "make it premium") and rejected patterns [56].
2. For large work, get a mock-up or storyboard approved first; for motion, agree what moves and why [56].
3. Name the medium and read its note under "Per medium". Render code at desktop and phone widths; view images, slides and ads at full size and as a thumbnail.
4. Scan Part A, then Part B. List every hit as `id: where: what is wrong`, for example `H16: .sub on hero: 3.2:1 contrast`. Measure the rendered result, not the CSS, and apply each rule only within its stated scope and medium.
5. Fix in this order: legibility and honest data (H12, H13, H16, H21, H27, H37), hierarchy (H5 to H10, H32), spacing and alignment (H1 to H4, H30), then type, colour and imagery, then Part B.
6. Keep the owner's style: a dark, playful or minimal design should get better at being itself.
7. Re-check. A fix that lands on another default is not a fix (T13), and nor is gutting the design: a landing page still needs a strong, visual first screen, the offer and one action; an ad or slide still needs its visual. Keep every real piece of content, including footers and legal lines. Add nothing the original or brief does not claim: no new features, details, numbers, data, customers or quotes, even in mock-ups and charts. No filler copy: no new taglines, intros or reassuring lines ("Built for how you work"); every new line carries a fact from the brief. If cutting hype leaves a stub or a line that repeats its heading, merge or drop it. Where decoration stood in for the product, give it a sized slot such as [product screenshot]; for a missing fact, a placeholder such as [customer quote]. No process notes in the design.
8. Run the final check. Report hits, changes, and anything left alone on purpose. Save the owner's corrections, and why, beside their approved examples [56].

## Part A: Hard rules

Style-agnostic.

### Spacing and alignment

H1. **Use a spacing scale.** Every margin, padding and gap from a short scale on a base unit (Material uses 8dp [37]), steps at least 25% apart [48]. Fix: snap odd values like 13px to 4, 8, 12, 16, 24, 32, 48, 64, 96.

H2. **Group by proximity.** Space within a group is clearly smaller than between groups; a heading sits closer to its content than to the section above [40][38]. Fix: tighten within, loosen between.

H3. **Share edges.** Align text, icons and images to a few common edges with a steady rhythm [37]. Fix: few distinct left edges.

H4. **Start with too much space.** Begin generous and remove space until it looks right; never stretch content to fill the screen [48].

### Hierarchy

H5. **One focal point.** Each view needs one most important thing, the biggest or highest-contrast element, and at most two large elements [38]. The squint test shows one first stop [38]; shrink, mute or remove what competes.

H6. **Three sizes, three contrasts.** At most three text sizes and three contrast levels in a view [38][39]; NN/g's example is body 14 to 16px, subheads 18 to 22px, headers up to 32px, and a poster or hero headline can be larger [38]. Fix: merge near-duplicates.

H7. **Weight and colour, not just size.** Two weights usually suffice (400 or 500, and 600 or 700); nothing under 400 for interface text [47].

H8. **De-emphasise to emphasise.** Mute competitors instead of making the key element louder [48].

H9. **One primary action.** One solid primary button per view; secondary as outline buttons, tertiary as links [47].

H10. **Front-load the words.** People scan the top lines and left edge [41], often only the first two words of a heading or list item [58]; 80% of fixations fall on the left half of a page [59]. Fix: key information first and left; headings and bullets open with the words that carry the meaning, so the page scans in layers [57].

### Typography

H11. **One or two typefaces.** Most designs can carry a second font; few a third [46]. Fix: one family, or two with fixed roles [46].

H12. **Line length 45 to 75 characters.** Body text reads best at 45 to 75 characters per line [45][44]; at most 80 at WCAG AAA [35]. Fix: `max-width: 65ch` to `70ch` [44].

H13. **Line height and size.** Body line spacing 120% to 145%; web body 15 to 25px [18][68]. Text must not clip when users set line height 1.5, paragraph spacing 2, letter spacing 0.12 and word spacing 0.16 times the font size [63]. Fix: body 16 to 18px, line height about 1.4 to 1.5, headings tighter; no fixed-height text boxes.

H14. **Use a hand-picked type scale.** Pick sizes from a short preset list, for example 12, 14, 16, 18, 20, 24, 30, 36, 48, 60, 72 [48].

H15. **Caps and quotes.** All caps only for labels under one line, with 5% to 12% extra letter spacing; caps paragraphs read about 13% slower [18][69]. Curly quotes; no letter spacing on lowercase body text [18]. Body text is flush left; full justification (both edges straight) only with hyphenation [68][35]. This rule is not about centring.

### Colour

H16. **Contrast floors.** Text 4.5:1; large text (24px, or 18.5px bold) 3:1 [32]. Controls, icons and chart marks 3:1 against neighbours, except inactive controls; a control with a passing label needs no 3:1 border [33]. Custom focus rings: at least 2px with a 3:1 change [64]. Measure every pair; 4.49:1 fails. WCAG 3 is still a draft [66], so APCA scores are advice, not a pass [67].

H17. **Small palette.** Simple designs use about two main and two secondary colours [38]. 60-30-10 is an interior-design rule of thumb, not a tested rule [55]; use it only as a starting split. Fix: main colour, neutrals, one accent.

H18. **Dark grey, not black, and real neutrals.** Start dark surfaces from a very dark grey such as Material's #121212 and plan 8 to 10 greys [48][76], tinted warm or cool to suit the main colour [48][49]. On dark surfaces, desaturate accents [76].

H19. **No grey text on colour.** Secondary text on a coloured background should be a lighter or darker shade of that hue, not grey or lowered opacity [47][49]. Then re-check H16.

H20. **Never colour alone.** Never carry meaning by colour only [38][65]; add text, an icon, pattern or underline. About 8% of men of European descent have red-green colour deficiency [70]: never rely on red against green; use blue with orange, or magenta with green [71][72].

### Imagery and composition

H21. **Text on images must pass.** Text over a photo or gradient needs 4.5:1 against the pixels behind it [32]. Fix: a scrim, a solid panel, or a calmer spot.

H22. **Show the real thing.** Users study real product and people photos and ignore decorative and stock images [42]. Fix: the actual product, place, team or work, or nothing.

H23. **Treat image sets alike.** One size, ratio, crop and treatment per set, as Material does for thumbnails [37].

H24. **Place the subject on purpose.** The rule of thirds barely predicts image quality [53]. Fix: crop to an obvious subject, with a calm area for copy.

H25. **Less is more appealing.** Low complexity and a genre-familiar layout are rated most appealing, judged within 50ms [50][51]; taste varies by country, age and education [52]. Familiar structure is good; generic styling is not (Part B).

### Copy on visuals, targets and consistency

H26. **One message per ad.** Ads and social posts only, never web heroes or slides. One message and one action; Meta recommends primary text of 1 to 3 lines (about 125 characters) and headlines of about 40 characters [54]. Detail goes in the caption.

H27. **Targets big enough.** Controls (not labels or badges) need at least 24 by 24 CSS px, or spacing [34]; Apple asks 44 by 44pt [36]. Measure the rendered box, not the padding value: a 48px-tall button passes whatever its padding says.

H28. **Same thing, same look.** Each role (button, card, link, heading level) has one style, following platform conventions [43].

H29. **Cut what does not help.** Extra elements compete with the ones that matter [43]; delete what does not help the reader understand or act, though chart titles and annotations that state the point do help [84][85].

### Structure and reading order

H30. **Build on a grid.** Column grid with fixed margins and gutters; blocks start and end on column edges [61][37].

H31. **Reading order matches visual order.** Source order matches the order people read [62].

H32. **The first screen carries the point.** About 57% of page viewing time is above the fold [60]: put the offer and action there, and let the next section peek in [60].

H33. **Numbers and punctuation.** Tabular figures where numbers are compared; en dashes for ranges, one space after a full stop [68]. No lone word on a headline's last line.

### Data visuals

H34. **Pick the chart by the task.** Position on a shared scale is read most accurately, then length, then angle and area; shading worst [77][78]. Fix: bars or dots to compare amounts, lines for change over time [87].

H35. **Colour scale matches the data.** Categories: distinct hues, 3 to 5 comfortable, over 8 fails [75][73]; ordered values: one hue light to dark; diverging only around a real midpoint [73]; no rainbow [74]. To stress one series, grey the rest [75].

H36. **No 3D, no dual axes.** Depth makes values slower and harder to read [82]; two y-axes let scales invent a relationship [83]. Pies only for part-to-whole with few flat slices [81].

H37. **Bars start at zero.** Length is the value, so bar axes start at zero and each bar ends on its value against the gridlines; truncation makes small gaps look large [79][80]. Line charts may zoom when change is the point [79].

H38. **Title states the finding.** "North grew most", not "Revenue by region"; people recall titles and annotations that carry the message [84][85]. Label marks directly, not in a legend; sort bars unless order matters; light gridlines [86][80].

### Slides

H39. **Sentence headline, visual evidence.** One point per slide, as a sentence headline of at most two lines, backed by a chart, image or diagram rather than bullets; recall rose from 69% to 79% [88][89]. Labels sit beside what they name [90].

H40. **Type that reads across a room.** Headline at least 28pt, body 18 to 24pt, callouts at least 14pt [89]. Keep the spoken script off the slide [90].

### Logos and icons

H41. **Logos work small and in one colour.** Check at 16 and 32px; drop detail that vanishes [96]. Supply one-colour and reversed versions, with clear space measured from a part of the mark [114]; favicons square and over 48px [113]. Moderately detailed, natural marks are recognised best [95].

H42. **One icon family.** One grid, stroke, corner style, size and perspective, weight matched to nearby text; pad asymmetric icons to centre them by eye [96][98]. App icons: no photos or thin strokes [97].

H43. **Label icons.** Few icons are understood without a word; pair them with text [99]. A sparkle does not reliably mean AI [100].

### Ads and social

H44. **Brand and product early, in the right frame.** Brand and product visible from the first frame, in the brand's own colours and shapes [93][94]. Build to the placement (4:5 feed, 9:16 Stories and Reels); keep key text and logos off the edges the app covers [91][92].

## Part B: AI tells

Defaults that read as generated. A tell is a pattern the model added, not one the brief chose; a gradient or card with a reason can stay [56]. Fix with something specific to the subject.

### Layout

T1. **Template hero.** Centred pill badge, big headline, one-line subhead, one or two buttons [3][24][31]. Fix: open with the most characteristic thing in the subject's world, such as the product or a real photo [2], sized to its content [26].

T2. **Three identical cards.** Three equal cards, each with an icon, two-word title and one line [3][24][26]. Fix: the real offer with specifics, sized by importance [26].

T3. **Section kit.** Stat banner, 1-2-3 steps, FAQ accordion, "Trusted by" logo bar, three pricing tiers [3][31]. Fix: only sections with real content.

T4. **Decoration instead of subject.** Glowing orbs, blobs, iridescent 3D shapes and dot grids where the product should be [24][31].

T5. **Placeholder icons and emoji.** The obvious icon in a tinted rounded square; rockets and bolts as bullets [3][24][31]. Fix: one fitting icon set, or none [26].

T6. **Motion on everything.** Every section fades up, every card lifts on hover [2][26][31]. Fix: one considered moment or responses to input; respect reduced motion [2][26].

T31. **Cards inside cards.** Boxes nested in boxes, each with its own border, fill or shadow [56]. Fix: one container level; group the inside with space and type (H2).

T32. **Diagram chrome.** Pulsing or glowing dots travelling along connector lines, and labels on things that need none [56]. Fix: connectors only for real flows, still unless motion explains a step (T6).

T33. **Bento grid by default.** A mosaic of mixed-size rounded tiles for content with no such shape [109][110]. Fix: layout that follows the content.

T34. **Hero clutter.** Floating badges, chips, stickers or cards in the hero [111]. Fix: brand, headline, one sentence, one action, one image [111].

T35. **Gimmick texture and motion.** Grid-paper backgrounds, logo marquees, bouncing buttons, blinking cursors, pulsing dots, confetti [110][109]. Fix: remove; keep motion that reports real state.

### Colour and effects

T7. **Purple-blue gradient.** Violet-to-indigo washes on hero or buttons, often with gradient headline text [1][3][24][31]. Fix: colour from the subject itself [26]; solid headline text.

T8. **Glassmorphism.** Translucent blurred panels over a gradient [3][24][31]. Fix: translucency only for real overlays.

T9. **Glows and sparkle.** Big coloured glows, sparkles for anything AI [100], shimmer on things not loading [3][31]. Fix: emphasis by size, weight, position and contrast [47].

T10. **One shadow and radius on everything.** The same soft shadow and radius everywhere [2][26][31]. Fix: elevation only for things above others; radius by role [26].

T11. **Accent stripes.** A coloured top or left border on each card [3][110]; once a human tip [48], now a tell. Fix: separate with space or type.

T12. **Dark mode with grey text.** Near-black background, mid-grey body text barely passing [2][3]. Fix: pick light or dark for the audience, then pass H16 [26].

T13. **Swapping to the next default.** Dodging purple into another stock look: cream, serif and terracotta, or near-black with acid green [2][109]. Told to avoid Inter, one model moved straight to Space Grotesk [1]. A bare text page is the same mistake. Fix: derive the look from the subject and brief [1][2].

### Type

T14. **Default fonts and the accent word.** Inter, Roboto or a system font for everything [1][3][4][31], or Space Grotesk, Instrument Serif or Geist, often with one italic or coloured headline word [1][2][3]. Fix: type chosen for the brief (H11).

T15. **Eyebrow labels.** Small tracked caps above each section ("FEATURES"), or 01, 02, 03 numbering on items with no order [2][3][110]. Fix: delete labels that repeat the heading.

T16. **Punctuation chrome.** Meta strings joined by middle dots, an arrow on every link [2], straight quotes [18]. Fix: plain words, curly quotes, arrows only for navigation.

### Imagery

T17. **Generated text and logos.** Gibberish signage, misshapen letters, a wrong letter in a logo [10][105]. Set all type and logos yourself.

T18. **The glossy AI look.** Oversaturated colour, exaggerated rim light, cinematic backgrounds, generic bokeh, overperfection [9][11][25]. Fix: art-direct to a real reference; a grain filter is not a fix [29].

T19. **Too-perfect faces.** Poreless, shiny, too-gorgeous faces [9][11]; AI faces are more average and attractive than real ones [28], and people spot them at chance [104]. Check for irregular pupils and mismatched catchlights [102][103]. Fix: real people (H22) or ordinary, specific faces.

T20. **Light, physics and anatomy that disagree.** Mismatched shadows, warped perspective, wrong reflections, fused fingers, teeth or glasses merging into the face [8][9][10][11][105]. Fix: check at 100% zoom. One odd detail is not proof; call an image generated only on two or more kinds of error, never on a detector alone [8][105].

T21. **Generic aspirational scenes.** A figure gazing into the distance, staged teamwork, scenes that could sell anything [25]. Fix: specific people, places and products [7] (H22).

T22. **The AI illustration look.** Faux-sketch or soft rendering over a generic pretty face, folds and perspective that break the style's rules [29][6]. Fix: illustration with a point of view, or generated art for concepts only.

T36. **Objects that could not work.** Straps melting into hands, meaningless dials, a product that changes between frames [8][101]. Fix: the real product (H22), or repair by hand [101].

### Copy

T23. **Headlines that sell anything.** "Revolutionize your workflow", "Unlock your potential" [26][31]. Fix: what only this business could say: what it is, for whom, a concrete detail [26].

T24. **AI vocabulary.** Seamless, elevate, supercharge, game-changing, cutting-edge, delve, vibrant [26][30][31]. Fix: plain verbs, concrete claims.

T25. **Stock sentence shapes.** "Not just X, it's Y" and triplets like "fast, simple and secure" [30]. Fix: one direct statement.

T26. **Default buttons and casing.** "Get started" [31], Title Case On Every Heading [30]. Fix: sentence case; buttons say what happens next ("See pricing").

T27. **Fake proof.** Round-number stat banners, star ratings, "Trusted by" logo bars, placeholder testimonials [3][31]. Fix: only real, attributable proof; otherwise leave it out, never invent it.

### Fit

T28. **Could belong to anyone.** Swap in a competitor's logo and nothing else needs to change [1][4][111]. Fix: show what only this subject has, from what the owner supplied.

T29. **AI imagery where trust matters.** Synthetic people, places or products in health, finance, travel or big purchases [15][16]; 62% of Americans reject AI-made people in ads even when disclosed [108]. US ads showing "actual consumers" must use real ones [106]; the EU requires deepfake labels from 2 August 2026 [107]. Fix: real photography or honest disclosure [13][14].

T30. **Shipping the first output.** One generation, no critique pass [26]; the only AI ad NIQ's viewers missed was heavily edited by professionals [12]. Fix: run this skill at full size and every crop.

T37. **Deck sameness.** Every slide alike: topic title, bullets, generic image [112]. Fix: one point per slide (H39), layout chosen by the evidence.

T38. **Chart decoration.** Gradient or glowing bars, rainbow series, a legend repeating the axis, shadows on marks, a truncated axis [74][79][86]. Fix: H34 to H38.

T39. **Stock-glyph logo.** A letter or stock icon in a gradient rounded square, or a sparkle as the mark [96][100]. Fix: a mark drawn for the name (H41).

## Per medium

Only where the rules differ.

- **Web and UI:** H9, H27, H30 to H32, T1 to T6, T33 to T35, at 1280px and 375px.
- **Social and ads:** H26, H44 and H21; not H32. Judge at feed thumbnail size.
- **Slides and posters:** H39, H40, T37; read at a distance. H9, H27 and H32 do not apply.
- **Charts:** H34 to H38 and T38 first, then H16 and H20.
- **Logos and icons:** H41 to H43, T39, at 16px, 32px and full size, in one colour.
- **AI images:** T17 to T22, T29, T36 at 100% zoom on hands, eyes, teeth, text and edges. Set words and logos as real type.

## Final check

1. Every text pair passes 4.5:1, large text 3:1, controls 3:1 (H16, H21).
2. One focal point survives the squint test; at most three text sizes and two typefaces (H5, H6, H11).
3. Body lines 45 to 75 characters, line height about 1.4 to 1.5 (H12, H13).
4. Spacing from the scale, groups by proximity, blocks on a grid, a few shared edges, sound at phone width (H1 to H3, H30).
5. One primary action per view; rendered targets at least 24 by 24 px (H9, H27).
6. Main colour, neutrals and one accent; no pure black (H17, H18).
7. Images carry information and match each other (H22, H23).
8. An ad shows one message and the brand at a glance (H26, H44).
9. A slide makes one point in a sentence headline (H39).
10. Bars start at zero; chart titles state the finding; marks labelled directly (H37, H38).
11. Logos and icons read at 16px and in one colour (H41).
12. No template hero, card trio, section kit, bento or decorative blobs (T1 to T4, T33).
13. No purple gradient, glass, glow or gradient text (T7 to T9, T14).
14. No emoji bullets, eyebrow labels, nested cards or default motion (T5, T6, T15, T31, T32, T35).
15. Every fact, number and data point traces to the brief or original; no filler line added (T23 to T27).
16. No fix swapped in another default, and the design could only be this one (T13, T28).
