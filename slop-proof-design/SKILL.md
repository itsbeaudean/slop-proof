---
name: slop-proof-design
description: Use when making, editing or reviewing any design, UI, web page, landing page, social graphic, ad or AI-generated image. Applies hard, sourced design rules and strips the default look of AI-made design.
---

# Slop-proof design

Make a design better in the style it already has: apply the hard rules, then remove the AI defaults.

Rule ids are stable; a removed rule leaves a gap. [n] points to SOURCES.md, and every number comes from its source.

## How to run it

1. Gather direction first: the brief, the owner's approved work and brand rules, with notes on what to follow ("use this spacing and type", not "make it premium") and which patterns they reject [56].
2. For new or large work, get a mock-up or storyboard approved before building everything; for motion, agree what moves, when, and what it explains [56].
3. Render code at desktop and phone widths; view images at full size and as a thumbnail.
4. Scan against Part A, then Part B. List every hit as `id: where: what is wrong`, for example `H16: .sub on hero: 3.2:1 contrast`. Measure the rendered result, not the CSS, and apply each rule only within its stated scope.
5. Fix in this order: legibility (H12, H13, H16, H21, H27), hierarchy (H5 to H10), spacing and alignment (H1 to H4), then type, colour and imagery, then Part B.
6. Keep the owner's style: a dark, playful or minimal design should get better at being itself.
7. Re-check. A fix that lands on another default is not a fix (T13), and nor is gutting the design: a landing page still needs a strong, visual first screen, the offer and one action, and should still look designed. Keep every real piece of content. Add nothing the original does not claim: no new features, product details, numbers, customers or quotes, including inside mock-ups and sample UI. Where decoration stood in for the product, give the real thing a sized slot, such as a framed [product screenshot]; where a fact is missing, use a short placeholder such as [customer quote]. Never write notes about your process into the design.
8. Run the final check. Report hits, changes, and anything left alone on purpose. Save the owner's corrections, and why, beside their approved examples for next time [56].

## Part A: Hard rules

Style-agnostic.

### Spacing and alignment

H1. **Use a spacing scale.** Take every margin, padding and gap from a short fixed scale built on a base unit (Material uses 8dp [37]), with steps at least about 25% apart [48]. Check: odd values like 13px or 22px. Fix: snap to a scale such as 4, 8, 12, 16, 24, 32, 48, 64, 96.

H2. **Group by proximity.** Space within a group is clearly smaller than between groups; a heading sits closer to its content than to the section above [40][38]. Fix: tighten within, loosen between.

H3. **Share edges.** Align text, icons and images to a few common edges with a steady rhythm [37]. Fix: few distinct left edges; left-align body text and centre only short lines [18].

H4. **Start with too much space.** Begin generous and remove space until it looks right; do not stretch content to fill the screen [48].

### Hierarchy

H5. **One focal point.** Each view needs one clearly most important thing, the biggest or highest-contrast element, and at most two large elements [38]. The squint test should show one first stop [38]; shrink, mute or remove what competes.

H6. **Three sizes, three contrasts.** No more than three text sizes and three contrast levels in a view [38][39]. NN/g's content-page example: body 14 to 16px, subheads 18 to 22px, headers up to 32px [38]; a landing-page or poster headline can be larger if the steps stay few and clear. Fix: merge near-duplicate sizes.

H7. **Weight and colour, not just size.** Two weights usually suffice (400 or 500, and 600 or 700); avoid weights under 400 for interface text [47].

H8. **De-emphasise to emphasise.** Mute competitors rather than making the key element louder [48].

H9. **One primary action.** One solid, high-contrast primary button per view; secondary actions as outline buttons, tertiary as links [47].

H10. **Front-load the words.** People scan text in an F-shape, favouring the top lines and left edge [41]. Fix: key information first; start headings with information-carrying words [41].

### Typography

H11. **One or two typefaces.** Most designs can carry a second font; few a third [46]. Fix: one family, or two with fixed roles (headings and body) [46].

H12. **Line length 45 to 75 characters.** Body text reads best at about 45 to 75 characters per line [45], 50 to 75 in Baymard's review [44]; no more than 80 at WCAG AAA [35]. Fix: `max-width: 65ch` to `70ch` [44].

H13. **Line height and size.** Body line spacing 120% to 145% of font size; web body text 15 to 25px [18]. Layouts must survive users setting line height to 1.5 and paragraph spacing to 2 times font size [35]. Fix: body 16 to 18px, line height about 1.4 to 1.5, headings tighter.

H14. **Use a hand-picked type scale.** Pick sizes from a short preset list, for example 12, 14, 16, 18, 20, 24, 30, 36, 48, 60, 72 [48].

H15. **Caps, quotes and alignment.** All caps only for short labels, with 5% to 12% extra letter spacing; curly quotes; no justified web text [18][35].

### Colour

H16. **Contrast floors.** Text needs 4.5:1, large text (18pt, or 14pt bold, roughly 24px or 18.5px) needs 3:1 [32]. Buttons, input borders, icons and chart marks need 3:1 against neighbours [33]. Measure every pair; 4.49:1 fails.

H17. **Small palette.** Simple designs use about two main and two secondary colours [38]. 60-30-10 is an interior-design rule of thumb, not a tested rule [55]; use it only as a starting split. Fix: main colour, neutrals, one accent.

H18. **Dark grey, not black, and real neutrals.** True black tends to look unnatural, so near-black is fine; start dark surfaces from a very dark grey and plan 8 to 10 grey shades [48], tinted warm or cool to suit the main colour [48][49].

H19. **No grey text on colour.** Secondary text on a coloured background should be a lighter or darker shade of that hue, not grey or lowered opacity [47][49]. Then re-check H16.

H20. **Never colour alone.** Do not carry meaning by colour only [38]; add text, an icon, weight or underline.

### Imagery and composition

H21. **Text on images must pass.** Text over a photo or gradient needs 4.5:1 against the pixels behind it [32]. Fix: a scrim, a solid panel, or a calmer spot.

H22. **Show the real thing.** Users study photos of real products and people and ignore decorative images and stock models [42]. Fix: the actual product, place, team or work, or nothing.

H23. **Treat image sets alike.** One size, ratio, crop and treatment per set, as Material does for thumbnails [37].

H24. **Place the subject on purpose.** The rule of thirds barely predicts how good people find an image [53]. Fix: crop to an obvious subject, with a calm area for copy.

H25. **Less is more appealing.** Low visual complexity and a genre-familiar layout are rated most appealing, a judgement formed within 50ms [50][51]. High complexity is generally disliked, though preference varies by country, age and education [52]. Familiar structure is good; generic styling is not (Part B).

### Copy on visuals, targets and consistency

H26. **One message per graphic.** For ads and social images, text should say what to do at a glance; Meta recommends primary text of 1 to 3 lines (about 125 characters) and headlines of about 40 characters [54]. Fix: one headline and one action; detail goes in the caption.

H27. **Targets big enough.** Links, buttons and other controls (not labels or badges) need targets of at least 24 by 24 CSS px [34]; Apple asks for 44 by 44pt [36].

H28. **Same thing, same look.** One style per role: every primary button, card, link and heading level looks and behaves the same, following platform conventions [43].

H29. **Cut what does not help.** Every extra element competes with the ones that matter [43]. Delete what does not help the reader understand or act.

## Part B: AI tells

Defaults that read as generated. A tell is a pattern the model added, not one the brief chose; a gradient or card with a reason can stay [56]. Fix each with something specific to the subject, not the next default.

### Layout

T1. **Template hero.** Centred pill badge, big headline, one-line subhead, one or two buttons [3][24][31]. Fix: open with the most characteristic thing in the subject's world, such as the product, a real photo or a specific headline [2], sized to its content [26].

T2. **Three identical cards.** Three equal cards, each with an icon, two-word title and one line [3][24][26]. Fix: the real offer with specifics, sized by importance [26].

T3. **Section kit.** Stat banner, 1-2-3 steps, FAQ accordion, "Trusted by" logo bar, three pricing tiers [3][31]. Fix: only sections with real content.

T4. **Decoration instead of subject.** Glowing orbs, blobs, iridescent 3D shapes and dot grids where the product should be [24][31].

T5. **Placeholder icons and emoji.** The obvious icon in a tinted rounded square; rockets and lightning bolts as bullets [3][24][31]. Fix: one icon set drawn for the job, or none [26].

T6. **Motion on everything.** Every section fades up, every card lifts on hover [2][26][31]. Fix: one considered moment or responses to input; respect reduced motion [2][26].

T31. **Cards inside cards.** Boxes nested in boxes, each with its own border, fill or shadow [56]. Fix: one container level; group the inside with space and type (H2).

T32. **Diagram chrome.** Pulsing or glowing dots travelling along connector lines, and labels on things that need none [56]. Fix: connectors only for real flows, still unless motion explains a step (T6).

### Colour and effects

T7. **Purple-blue gradient.** Violet-to-indigo washes on hero or buttons, often with gradient headline text [1][3][24][31]. Fix: colour from the subject itself [26]; solid headline text.

T8. **Glassmorphism.** Translucent blurred panels with a faint border over a gradient [3][24][31]. Fix: translucency only for real overlays.

T9. **Glows and sparkle.** Big coloured glows, sparkles for anything AI, shimmer on things not loading [3][31]. Fix: emphasis by size, weight, position and contrast; at most a small offset shadow [47].

T10. **One shadow and radius on everything.** The same soft shadow under every card and one radius everywhere [2][26][31]. Fix: elevation only for things above others; radius by role [26].

T11. **Accent stripes.** A coloured top or left border on each card [3]. Once a human design tip [48], it now reads as generated. Fix: separate with space, type or a real visual.

T12. **Dark mode with grey text.** Near-black background, medium-grey body text barely passing [2][3]. Fix: choose light or dark for the audience, then pass H16 [26].

T13. **Swapping to the next default.** Dodging purple into another stock look: cream, serif and terracotta, or near-black with acid green [2]. Told to avoid Inter, one model moved straight to Space Grotesk [1]. Over-correcting into a bare text page is the same mistake. Fix: derive the look from the subject and brief, then compare with these clusters [1][2].

### Type

T14. **Default fonts and the accent word.** Inter, Roboto or a system font for everything [1][3][4][31], or Space Grotesk, Instrument Serif or Geist, often with one italic or coloured headline word [1][2][3]. Fix: type chosen for the brief (H11); the whole headline carries the voice.

T15. **Eyebrow labels.** Small tracked caps above each section ("FEATURES") [2][3]. Fix: delete labels that repeat the heading.

T16. **Punctuation chrome.** Meta strings joined by middle dots, an arrow on every link and button [2], straight quotes [18]. Fix: plain language, curly quotes, arrows only for real navigation.

### Imagery

T17. **Generated text and logos.** Gibberish signage, misshapen letters, a wrong letter in a logo [10]. Set all type and logos yourself.

T18. **The glossy AI look.** Oversaturated colour, exaggerated rim light, cinematic backgrounds, generic bokeh, overperfection [9][11][25]. Fix: art-direct to a real reference with believable light; a grain filter is not a fix [29].

T19. **Too-perfect faces.** Poreless, shiny, too-gorgeous faces [9][11]; AI faces are more average and attractive, and less memorable, than real ones [28]. Fix: real people (H22) or ordinary, specific faces.

T20. **Light, physics and anatomy that disagree.** Mismatched shadows, warped perspective, wrong reflections, patched backgrounds, fused fingers [8][9][10][11]. Fix: check at 100% zoom.

T21. **Generic aspirational scenes.** A vague figure gazing into the distance, staged teamwork, scenes that could sell anything [25], as stock does. Fix: specific people, places and products [7] (H22).

T22. **The AI illustration look.** Faux-sketch or soft rendering over a generic pretty face, folds and perspective that break the style's own rules [29]; AI errors look random rather than like human slips [6]. Fix: illustration with a point of view, or generated art for concepts only.

### Copy

T23. **Headlines that sell anything.** "Revolutionize your workflow", "Unlock your potential", "Build the future of X" [26][31]. Fix: the sentence only this business could say: what it is, for whom, a concrete detail [26].

T24. **AI vocabulary.** Seamless, elevate, supercharge, game-changing, cutting-edge, delve, vibrant [26][30][31]. Fix: plain verbs, concrete claims.

T25. **Stock sentence shapes.** "Not just X, it's Y" and triplets like "fast, simple and secure" [30]. Fix: one direct statement; two specific points beat three vague ones.

T26. **Default buttons and casing.** "Get started", "Try it free" [31], Title Case On Every Heading [30]. Fix: sentence case; button text that says what happens next ("See pricing").

T27. **Fake proof.** Round-number stat banners, "Trusted by" logo bars, placeholder testimonials [3][31]. Fix: only real, attributable numbers, quotes and logos; otherwise leave them out, and never invent replacements.

### Fit

T28. **Could belong to anyone.** Swap in a competitor's logo and nothing else needs to change [1][4]. Fix: show what only this subject has (its work, data, place and voice), from what the owner supplied.

T29. **AI imagery where trust matters.** Synthetic people, places or products in health, finance, government, travel or big purchases, where penalties are strongest [15][16]. Fix: real photography or honest disclosure [13][14].

T30. **Shipping the first output.** One generation, no critique pass [26]; the only AI ad NIQ's viewers did not spot was heavily edited by professionals [12]. Fix: run this skill at full size and every crop.

## Final check

1. Every text pair passes 4.5:1, large text 3:1, controls 3:1 (H16, H21).
2. One clear focal point survives the squint test (H5).
3. No more than three text sizes and two typefaces in a view (H6, H11).
4. Body lines 45 to 75 characters, line height about 1.4 to 1.5 (H12, H13).
5. All spacing from the scale; groups read by proximity (H1, H2).
6. Content shares a few clear edges and holds up at phone width (H3).
7. One primary action per view (H9).
8. Main colour, neutrals and at most one accent; no pure black (H17, H18).
9. Images carry information and match each other (H22, H23).
10. A graphic gets its message across at a glance (H26).
11. Targets at least 24 by 24 px (H27).
12. No template hero, card trio, section kit or decorative blobs (T1 to T4).
13. No purple gradient, glass, glow or gradient text (T7 to T9, T14).
14. No emoji bullets, eyebrow labels, nested cards or default motion (T5, T6, T15, T31, T32).
15. Copy is specific and true; every fact and claim traces to the brief or original (T23 to T27).
16. No fix swapped in another default, and the design could only be this one (T13, T28).
