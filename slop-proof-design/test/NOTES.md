# Test notes

Three deliberately sloppy samples: a landing page for a made-up product (`before.html`), a 4:5 social ad (`social-before.html`, brief in `social-brief.txt`) and a one-slide chart (`slide-before.html`, brief in `slide-brief.txt`). Each run gave an AI agent (headless, no tools) the skill, the brief and the file in one prompt and asked for a hit list and a fixed file. Pages were rendered in headless Chrome at 1280px and 375px, the ad at 1080 by 1350 and the slide at 1920 by 1080. Every figure below was measured from the rendered result (computed styles, WCAG contrast of each text element against its real background, rendered box sizes), not estimated.

## Current results

Skill version: the one in this folder (44 hard rules, 39 tells).

### Landing page (`after.html`, `hits.txt`)

| Measure | Before | After |
| --- | --- | --- |
| Problems caught | | 44 (21 hard rules, 23 AI tells) |
| Distinct rendered font sizes | 9 (12 to 64px) | 3 (16, 20, 48px; 32px headline on phones) |
| Distinct text colours | 5, one gradient-clipped | 4, all solid |
| Background fills | 6 (4 gradients, 2 translucent glass) | 2 solid |
| Emoji | 8 | 0 |
| Animated elements | 22 | 0 |
| Words of copy | 118 | 64 |
| Lowest text contrast | 70% white on a pink gradient (fails) | 6.25:1 |
| Primary button, rendered | | 189 by 48px |

Invented content: none. The fake logo bar, the 10K+, 99.9% and 4.9 stats and the gradient were removed, not replaced. The empty hero became a framed `[product screenshot]` slot beside the headline, offer and one primary action. All three features, the benefits list and the closing call to action stayed. The earlier false positives are gone: H26 was not applied to the hero and H27 was not flagged from padding.

Misses: cutting the hype left thin copy. "Connect your favourite tools" now repeats as heading and body, and "Unleash your team's creativity" became the stub "Your team's creativity". The H15 hit also mentions centred body text, which H15 says is not its concern. Step 7 now says to merge or drop stubs and repeats.

### Social ad (`social-after.html`, `social-hits.txt`)

| Measure | Before | After |
| --- | --- | --- |
| Problems caught | | 34 (15 hard rules, 19 AI tells) |
| Distinct font sizes | 8 (16 to 92px) | 3 (20, 24, 60px) |
| Emoji | 11 | 0 |
| Words | 48 | 29 |
| Text over gradients and orbs | all of it | none; lowest contrast 9.09:1 |

The headline is now the brief's main fact ("Grinds and brews a cup in about 2 minutes"), with the app feature, the price on the button and the 1 March pre-order date. The five stars, "50,000+ coffee lovers", "Sustainable" and "AI-powered" claims are gone and nothing new was added. The orbs became a large `[product photo]` slot, so the ad keeps its visual.

Misses: the brand name is a small 20px label, weaker than H44 asks for. The ad is flat until a real product photo goes in.

### Slide (`slide-after.html`, `slide-hits.txt`)

| Measure | Before | After |
| --- | --- | --- |
| Problems caught | | 40 (20 hard rules, 20 AI tells) |
| Value axis | starts at 4.0, so West (4.1) is drawn at 20% of North (4.96) | starts at 0 |
| Title | "Driving Growth Through Innovation" | "North grew most because of the new Brisbane depot" |
| Bars | four rainbow gradients with glows and a legend | sorted, North in one colour, the rest grey, values on the bars |
| Distinct font sizes | 6 (14 to 60px) | 2 (24, 48px) |
| Lowest text contrast | about 2.5:1 (footer) | 7.38:1 |
| Words | 74 | 28 |

All four values match the brief and the title is the brief's finding. The six filler bullets, including claims not in the brief ("record-breaking", "customer satisfaction remained strong"), were removed.

Misses: the bars are scaled to the plot height minus 32px while the gridlines use the full height, so each bar ends about 5% short of its value against the axis (North reads near 4.73). H37 now says each bar must end on its value. The "Confidential, internal use only, Q3 FY26" footer was dropped; step 7 now names footers and legal lines as content to keep. The chart fills only the left half of the plot.

## Run 5 (`run5-*`): before the latest rule changes

45 hits. Fonts 9 to 3, emoji 8 to 0, animated elements 22 to 0, words 118 to 109, lowest contrast 8.98:1, nothing invented. False positives: H26 applied to the landing-page hero, H27 flagged from CSS padding (rendered buttons were 48 to 50px tall), and an H15 hit that called centred text "justified". Some filler copy crept in ("Built for how teams actually work"). These led to the scoped H26, the rendered-box wording in H27, the reworded H15 and the no-filler-copy rule.

## Run 1 (`run1-*`): over-correction

45 hits (24 hard rules, 21 tells), three of them wrong: H18 flagged a near-black background, H27 a badge that is not a control, and H26 was applied to the hero.

The fix went too far. It deleted almost everything, shrank the headline to 32px by treating NN/g's content-page example as a cap, and wrote notes about its own process into the page copy. Legible, but an empty text page rather than a better landing page. This led to the rule that gutting a design is not a fix, the scoping of H6, H18, H26 and H27, and T13's line about bare text pages.

## Run 2 (`run2-*`): invented product details

41 hits (19 hard rules, 22 tells), no false positives. It kept the dark style, cut to a tight type scale and removed the fake proof. But it built a product mock-up full of things the original never claimed: a board with columns and tickets, guest permissions and workspaces. Words of copy went from 118 to 234. This led to the rule to add nothing the original does not claim, including inside mock-ups and sample UI.

## Run 3 (not kept)

With the no-invention rule in place it invented nothing, but drifted back towards a bare text page with no visual on the first screen (82 words, no product area). Step 7 now asks for a strong, visual first screen and a sized slot for the real product where decoration stood in for it. Run 5 above came after that change.
