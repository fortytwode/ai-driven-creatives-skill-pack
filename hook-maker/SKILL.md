---
name: hook-maker
description: Generate ad hooks (text overlays, verbal opening lines, static display headlines) for paid social ads on Meta or TikTok. Uses the 3C Principle (Context, Clarity, Curiosity) and the 4-Layer Hook System (Visual, Text, Verbal, Audio). Refuses generic AI-ad-copy patterns like fragment stacking, statements that give the answer, and product names in the hook. Use when drafting hooks for direct-response subscription app ads.
---

# Hook Maker

Generate ad hooks across the three hook layers (text, visual, spoken) using RocketShip HQ's frameworks.

## When invoked

Ask the user three questions in order:

1. **What's the app and category?** (e.g., a sleep tracking app, a finance/budgeting app, a meditation app)
2. **What's the user problem?** (e.g., people don't trust their sleep score and don't know what to change)
3. **Which hook layer do you want?** (text overlay, verbal opening line, static display headline, or "credential + contradiction" pattern)

Then load the corresponding prompt from `prompts/`:

| Layer | Prompt file |
|---|---|
| Text overlay (video first frame) | `prompts/text-overlay-maker.md` |
| Verbal opening (first VO line) | `prompts/verbal-hook-maker.md` |
| Static display (single frame) | `prompts/static-display-maker.md` |
| Credential + contradiction pattern | `prompts/credential-contradiction-maker.md` |

Run the prompt with the user's inputs substituted into the placeholders. Generate 8 to 10 variants. After generating, briefly note which patterns are represented (per the rules in each prompt).

## The 3C Principle (every hook needs all three)

- **Context.** Who is this for, what category does it sit in. The brain has to categorize the content instantly or it scrolls.
- **Clarity.** What is this video about, why is it worth watching the next two seconds.
- **Curiosity.** An open loop. Tension, a contrarian angle, an implied mistake, an unresolved outcome.

Demand all three by name in the prompt. Models will happily generate hooks with curiosity and no clarity, or clarity and no context.

## The 4-Layer Hook System

Strong hooks operate across four layers at once.

| Layer | Role | Key question |
|---|---|---|
| Visual | Stops the scroll | How do I interrupt the feed? |
| Text | Orients the viewer | What is this about, why should I care? |
| Verbal | Builds connection | What is the story or argument? |
| Audio | Amplifies emotion | What should the viewer feel? |

When prompting AI, brief one layer at a time. Models are bad at multi-layer coherence and good at single-layer variants.

## Hard rules across all hooks

- First-person POV by default. Second-person ("you") only for direct challenges.
- Curiosity gap: the hook is the setup, never the reveal.
- 14 to 20 words for video text overlays; under 15 words for static display.
- No stacked fragments. "One app. One tap." reads like a robot.
- No product name in the hook.
- No generic CTAs ("Download now", "Try free").
- No em dashes or en dashes.
- Must satisfy all three of Context, Clarity, Curiosity.

## After generating

Offer to:
1. Generate variants in a different layer
2. Run the variants through the curation checklist (invoke `creative-curator` skill)
3. Build a script around the winning hook (invoke `script-maker` skill)
