# Beau Dean's skills

Skills for AI agents that find and fix AI slop. Each skill is a folder with a `SKILL.md` that any agent able to read a skill file can use. This repo is where I keep them and update them.

## slop-proof-design

Anti-slop for design. It tells an AI agent what to avoid in a design. It doesn't design and it doesn't set a style: the brief, the brand and your taste decide the look.

It covers web pages and UI, social graphics and ads, slides, charts, logos and icons, and AI-generated images and video. It has 114 avoids in 12 areas:

| Area | Avoids |
| --- | --- |
| X. Content and honesty (all media) | 8 |
| L. Layout and spacing | 14 |
| Y. Type | 12 |
| C. Colour and contrast | 9 |
| M. Motion and effects | 8 |
| U. Interface and interaction | 13 |
| W. Words on the design | 6 |
| P. Photos, AI images and video | 16 |
| D. Charts | 11 |
| S. Slides | 7 |
| G. Logos and icons | 6 |
| A. Ads and social | 4 |

Each avoid says what the problem looks like, why it hurts or reads as AI-made, and how to spot it. Each is tagged:

- **Floor** (30): accessibility, legibility or honesty, such as contrast under 4.5:1, text that clips, motion you can't stop, or invented numbers. Always a hit.
- **Rule** (46): a sourced usability or craft failure, such as body text under 16px on the web, three or more typefaces, a truncated bar axis or a hidden menu on desktop. A hit unless the brief breaks it on purpose.
- **Tell** (38): a default that reads as AI-made, such as the template hero, three identical cards, purple gradients, eyebrow labels, too-perfect faces or an orb logo. One alone is fine if chosen; several together read as generated.

It keeps up with current tools. Avoids marked **New** come from sources published between May and October 2026: the untouched shadcn and Lucide kit that vibe-coding builders ship, monospace pre-headings, forms that say thanks without sending, video that drifts between frames, infographics with facts baked into a generated image, and AI decks with flattened hierarchy. It also warns that current image and video models have dropped the old giveaways, so a clean image proves nothing.

Use it two ways: as guardrails loaded before an agent designs anything, or as a review pass that lists hits as `id: where: what` (for example `C1: .sub on hero: 3.2:1`). The agent may propose the smallest fix for each hit. It must not invent facts, swap one default for another, or strip real content.

`SOURCES.md` lists all 147 sources, each labelled as research, industry research, a standard or platform guideline, practitioner advice or journalism, with the ids that cite it.

## Install

Give this to your agent:

```text
Install the slop-proof-design skill from https://github.com/itsbeaudean/slop-proof. Copy the slop-proof-design folder into your skills folder. If you don't have a skills folder, save the contents of slop-proof-design/SKILL.md as a skill called slop-proof-design. Use it whenever you make, edit or review a design.
```

Or do it yourself: clone the repo and copy the `slop-proof-design` folder into your agent's skills folder.

```
git clone https://github.com/itsbeaudean/slop-proof.git
```

To get updates, pull the repo again or ask your agent to reinstall the skill.

## Use

- "Use slop-proof-design as guardrails while you build this page."
- "Review this ad against slop-proof-design and list the hits by id."
- "Run slop-proof-design on `index.html` and propose the smallest fix for each hit."

## Credit

The format is modelled on the `unslop` writing skill by Lauren Tan, part of the pstack plugin ([cursor/plugins](https://github.com/cursor/plugins/tree/main/pstack), MIT licence).

## Licence

MIT. See `LICENSE`.
