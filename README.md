# slop-proof

Skills for AI agents (Claude Code, Cursor, Grok Bot) that find and fix AI slop. Design first; LinkedIn and writing skills are coming soon.

## slop-proof-design

A skill that makes a design better in the style it already has, and stops it looking AI-made. It works on web pages, UI, social graphics, ads and AI images.

It gives the agent:

- **29 hard rules** (H1 to H29) on spacing, hierarchy, type, colour, imagery, copy and targets. Every number comes from a cited source, such as WCAG contrast ratios, NN/g research and Material guidelines.
- **32 AI tells** (T1 to T32): the template hero, three identical cards, purple gradients, glass, glows, emoji bullets, eyebrow labels, cards inside cards, fake stats and logo bars, stock headlines and more.
- **A workflow**: gather the brief and approved examples, review a mock-up before building, render and scan, list hits by rule id, fix in priority order, then run a 16-point final check.
- **Guard rails**: keep the owner's style, never gut the design, and never invent features, numbers, customers or quotes. Missing facts get a short placeholder such as `[customer quote]`.

`SOURCES.md` lists all 56 sources and says which ones are practitioner advice rather than research.

## Install

**Claude Code.** Copy the `slop-proof-design` folder into your skills folder:

```
git clone https://github.com/itsbeaudean/slop-proof.git
mkdir -p ~/.claude/skills
cp -r slop-proof/slop-proof-design ~/.claude/skills/
```

For one project only, copy it to `.claude/skills/slop-proof-design/` inside the project instead.

**Cursor.** Copy the folder to `~/.cursor/skills/slop-proof-design/` for all projects, or `.cursor/skills/slop-proof-design/` inside one project. Cursor also reads `~/.claude/skills/`, so the Claude Code install works for both.

**Grok Bot.** Paste the contents of `slop-proof-design/SKILL.md` into a chat and ask: "Save this as a skill called slop-proof-design." It works in any other chat agent too; paste it at the start of the chat when you need it.

## Use

- "Use slop-proof-design on this" and attach a screenshot, image or file.
- "Run slop-proof-design on `index.html`", or point it at a component or folder.
- "Review this ad against slop-proof-design, list the hits by rule id, then fix them."

The agent lists each hit as `id: where: what is wrong` (for example `H16` for contrast or `T7` for the purple gradient), fixes them in order, checks it did not swap in another default, and runs the final check. Give it your brand rules and examples of approved work for better results.

## What the test caught

`slop-proof-design/test/` has a deliberately sloppy landing page and the fixed versions from Grok Build, run headless. Counts are measured from the rendered pages.

- **Current result:** 45 problems caught (23 hard rules, 22 tells). Font sizes went from 9 to 3, background fills from 6 (4 gradients, 2 glass) to 2 solid, emoji from 8 to 0 and animated elements from 22 to 0. The lowest text contrast is now 8.98:1. It invented nothing, and the page kept its first screen, offer, sections and one primary action, with a slot for the real product screenshot.
- **Run 1 over-corrected.** It deleted almost everything and left a bare text page with notes about its own process in the copy. That is why the skill now says gutting a design is not a fix.
- **Run 2 invented things.** Its product mock-up showed boards, guest permissions and workspaces the original never claimed. That is why the skill now says to add nothing the original does not claim, mock-ups included.
- **Still imperfect:** the current run applied two rules outside their scope and added some filler copy. See `test/NOTES.md` for the full list.

The rules are floors, not taste. They lift most designs, but they will not replace a designer's judgement.

## More skills coming

LinkedIn and writing skills will follow in this repo.

## Credit

The format is modelled on the `unslop` writing skill by Lauren Tan, part of the pstack plugin ([cursor/plugins](https://github.com/cursor/plugins/tree/main/pstack), MIT licence).

## Licence

MIT. See `LICENSE`.
