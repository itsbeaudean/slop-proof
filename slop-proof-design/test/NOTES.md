# Test notes

`before.html` is a deliberately sloppy landing page for a made-up product, FlowSync. Each run gave Grok Build (headless, no tools) the skill and `before.html` in one prompt and asked for a hit list and a fixed page. Screenshots are full-page headless Chrome at 1280px wide. Counts below were measured from the rendered pages (computed styles of visible text), not estimated.

## Current result (`after.*`, `hits.txt`)

Skill version: the one in this folder.

| Measure | Before | After |
| --- | --- | --- |
| Problems caught | | 45 (23 hard rules, 22 AI tells) |
| Distinct rendered font sizes | 9 (12, 14, 16, 18, 20, 24, 40, 48, 64px) | 3 (16, 24, 48px) |
| Distinct text colours | 5, one of them gradient-clipped text | 4, all solid |
| Background fills | 6 (4 gradients, 2 translucent glass) | 2 solid |
| Emoji | 8 | 0 |
| Animated elements | 22 | 0 |
| Words of copy | 118 | 109 |
| Page height | 2,625px | 1,498px |
| Lowest text contrast | 70% white on a pink gradient (fails) | 8.98:1, white on the violet button |

Invented content: none. Every claim on the page traces to the original (beta, all-in-one platform, AI-powered workflows, speed, tool connections, bank-grade security, the three perks, free trial). The fake logo bar, the 10K+, 99.9% and 4.9 stats and the gradient were removed and not replaced with new ones. The empty gradient hero became a framed `[product screenshot]` slot.

Gutting: no. It kept a two-column first screen with headline, offer, one filled primary action, a text link and the product slot, plus all three sections and the closing call to action. It holds up at phone width.

Misses and false positives:
- H26 was applied to the landing-page hero, although the rule says it is for ads and social images.
- H27 was flagged from CSS padding; the rendered buttons are 146 to 229px wide and 48 to 50px tall, so they pass.
- H15 also claimed the body was "justified by centering", which is not what justified means. The caps-label part of that hit was right.
- Some filler copy crept in: "What FlowSync already offers teams." and "Built for how teams actually work". Not invented facts, but weak (T23).
- It kept a solid violet accent. Defensible as the owner's colour, close to T7.

## Run 1 (`run1-*`): over-correction

45 hits (24 hard rules, 21 tells), three of them wrong: H18 flagged a near-black background, H27 a badge that is not a control, and H26 was applied to the hero.

The fix went too far. It deleted almost everything, shrank the headline to 32px by treating NN/g's content-page example as a cap, and wrote notes about its own process into the page copy. Legible, but an empty text page rather than a better landing page. This led to the rule that gutting a design is not a fix, the scoping of H6, H18, H26 and H27, and T13's line about bare text pages.

## Run 2 (`run2-*`): invented product details

41 hits (19 hard rules, 22 tells), no false positives. It kept the dark style, cut to a tight type scale and removed the fake proof. But it built a product mock-up full of things the original never claimed: a board with columns and tickets, guest permissions and workspaces. Words of copy went from 118 to 234. This led to the rule to add nothing the original does not claim, including inside mock-ups and sample UI.

## Run 3 (not kept)

With the no-invention rule in place it invented nothing, but drifted back towards a bare text page with no visual on the first screen (82 words, no product area). Step 7 now asks for a strong, visual first screen and a sized slot for the real product where decoration stood in for it. The current result above is the run after that change.
