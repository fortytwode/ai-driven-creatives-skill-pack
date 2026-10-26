# AI-Driven Creatives Skill Pack

Four agent-like skills for building AI-driven ad creatives that perform on Meta and TikTok in 2026, plus the underlying prompts, frameworks, and checklists. Companion download to [The Ultimate Guide to AI-Driven Creatives](https://www.rocketshiphq.com/ultimate-guide-ai-driven-creatives/) by RocketShip HQ.

## What's inside

Four skills:

| Skill | What it does |
|---|---|
| **hook-maker** | Generates ad hooks across text, visual, and spoken layers using the 3C Principle and the 4-Layer Hook System. |
| **script-maker** | Generates direct-response scripts using the Setup / Shift / Proof / Payoff structure. Avoids autopilot PAS, BAB, AIDA templates. |
| **visual-director** | Builds production-ready prompts for Midjourney, Gemini image models, Kling or Gemini Omni Flash, Runway Gen-4.5, and ElevenLabs. |
| **creative-curator** | Walks any concept through three phases: drafting (before generation), production (during), curation (before shipping). |

Each skill is self-contained: a `SKILL.md` entry point plus the underlying prompts or checklists.

## Two ways to use

### As Claude Code skills

Drop the four skill folders into `~/.claude/skills/`:

```bash
git clone https://github.com/fortytwode/ai-driven-creatives-skill-pack.git
cp -r ai-driven-creatives-skill-pack/{hook-maker,script-maker,visual-director,creative-curator} ~/.claude/skills/
```

Restart Claude Code. Each skill becomes invokable when the description matches a request (e.g., "generate hooks for my fitness app" triggers `hook-maker`).

### As standalone prompts

Each skill folder contains a `prompts/` (or `checklists/`) directory with the underlying prompts. Open any `.md` file, copy the contents, paste into Claude / ChatGPT / Gemini / your tool of choice, fill in the bracketed placeholders.

## The frameworks behind the skills

- **3C Principle** (Context, Clarity, Curiosity): every hook needs all three in the first second. Lives in `hook-maker/SKILL.md`.
- **4-Layer Hook System** (Visual, Text, Verbal, Audio): the strongest hooks stack layers intentionally. Lives in `hook-maker/SKILL.md`.
- **Setup / Shift / Proof / Payoff**: the four-beat DR script structure, constrained by the bet and the body craft. Lives in `script-maker/SKILL.md`.
- **The eight iteration axes**: messaging, background, duration, music, VO, animation, scene order, visual hook treatment. Lives in `creative-curator/SKILL.md`.
- **The negative-space rule**: tell the AI what NOT to do; the forbidden list is the brief. Lives in `visual-director/SKILL.md`.

## Changelog

- **v1.1.0 (October 2026):** script-maker moves from Before / After / Now / Punchline to Setup / Shift / Proof / Payoff, matching the guide; `banp-script-maker.md` is now `script-maker.md`. Sora 2 (shut down 24 September 2026) replaced by Kling Video 3.0 or Gemini Omni Flash; `sora-transformation-clip.md` is now `transformation-clip.md`.

## License

MIT. Use freely. Attribution to RocketShip HQ appreciated but not required.

## Built by

[RocketShip HQ](https://www.rocketshiphq.com). Mobile user acquisition and creative strategy for subscription apps. 50,000+ ads made, $100mm+ in ad spend managed. Meta, Google, and TikTok partner.

Read the full guide: [The Ultimate Guide to AI-Driven Creatives](https://www.rocketshiphq.com/ultimate-guide-ai-driven-creatives/)
