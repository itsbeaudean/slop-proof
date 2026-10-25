# slop-proof

Skills for AI agents that find and fix AI slop. They work with any agent that can read a skill file. Design first; LinkedIn and writing skills are coming soon.

## slop-proof-design

Like the `unslop` writing skill, but for design. It makes a design better in the style it already has, and stops it looking AI-made. It works on anything visual: social graphics, ads, web pages, UI and AI images.

It gives the agent:

- **29 hard rules** (H1 to H29) on spacing, hierarchy, type, colour, imagery, copy and targets. Every number comes from a cited source, such as WCAG contrast ratios, NN/g research and Material guidelines.
- **32 AI tells** (T1 to T32): the template hero, three identical cards, purple gradients, glass, glows, emoji bullets, eyebrow labels, cards inside cards, fake stats and logo bars, stock headlines and more.
- **A workflow**: gather the brief and approved examples, review a mock-up before building, render and scan, list hits by rule id, fix in priority order, then run a 16-point final check.
- **Guard rails**: keep the owner's style, never gut the design, and never invent features, numbers, customers or quotes. Missing facts get a short placeholder such as `[customer quote]`.

`SOURCES.md` lists all 56 sources and says which ones are practitioner advice rather than research.

## Install

Clone the repo and copy the `slop-proof-design` folder into your agent's skills folder:

```
git clone https://github.com/itsbeaudean/slop-proof.git
```

If your agent doesn't have a skills folder, paste the contents of `slop-proof-design/SKILL.md` at the start of the chat, or ask it to save it as a skill.

## Use

- "Use slop-proof-design on this" and attach a screenshot, image or file.
- "Run slop-proof-design on `index.html`", or point it at a component or folder.
- "Review this ad against slop-proof-design, list the hits by rule id, then fix them."

The agent lists each hit as `id: where: what is wrong` (for example `H16` for contrast or `T7` for the purple gradient), fixes them in order, checks it did not swap in another default, and runs the final check. Give it your brand rules and examples of approved work for better results.

The rules are floors, not taste. They lift most designs, but they will not replace a designer's judgement.

## More skills coming

LinkedIn and writing skills will follow in this repo.

## Credit

The format is modelled on the `unslop` writing skill by Lauren Tan, part of the pstack plugin ([cursor/plugins](https://github.com/cursor/plugins/tree/main/pstack), MIT licence).

## Licence

MIT. See `LICENSE`.
