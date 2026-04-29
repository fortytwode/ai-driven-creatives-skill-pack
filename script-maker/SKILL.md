---
name: script-maker
description: Generate direct-response ad scripts using the Before / After / Now / Punchline (BANP) structure. Refuses PAS, BAB, AIDA defaults. Enforces 45-65 word length, conversational first-person tone, and the read-aloud test. Use when drafting video ad scripts for subscription apps.
---

# Script Maker

Generate ad scripts using RocketShip HQ's BANP (Before / After / Now / Punchline) structure.

## When invoked

Ask:

1. **App and category?**
2. **User problem?**
3. **Concept angle for this script?** (one-line emotional hook or contrarian framing)
4. **Audience?** (specific segment, e.g., "ESL professionals", "parents of neurodivergent kids", "marathon runners with insomnia")
5. **Mode?** (one of: 3 BANP variants from one brief, rewrite a flat AI-generated script, 3 audience-segment variants of the same concept)

Then load the corresponding prompt:

| Mode | Prompt file |
|---|---|
| 3 BANP variants from one brief | `prompts/banp-script-maker.md` |
| Rewrite a flat AI-generated script | `prompts/flat-script-rewriter.md` |
| 3 audience segment variants | `prompts/audience-segment-maker.md` |

For verbal hooks (first VO line, separate from a full script), invoke the `hook-maker` skill instead.

## The BANP structure

Four parts, in order:

1. **Before:** what life looked like before the user found the product
2. **After:** the shift, what changed when they found it
3. **Now:** the specific behavior or result today
4. **Punchline:** a memorable closer that reinforces the value

Example for a productivity app that records meetings:

- Before: "I used to spend 20 minutes after every meeting trying to remember what was said."
- After: "Now I just hit record on my phone and slip it in my pocket."
- Now: "It transcribes everything and gives me a perfect summary."
- Punchline: "My coworkers think I have a photographic memory. I don't correct them."

## Hard rules

- 45 to 65 words per script. Never exceed 70.
- Conversational, first-person.
- Flowing sentences. No stacked fragments.
- No sentence starts with the product name.
- Do NOT use PAS, BAB, AIDA, or any other framework. Only BANP.
- No em dashes or en dashes.
- Each variant must pass the read-aloud test (no dangling phrases, no broken fragments, no missing context).

## The read-aloud test (mandatory before shipping)

Read each variant out loud at natural pace. If you stumble, rewrite. Catch:

- **Dangling phrases.** "Every action item, pulled out." reads incomplete.
- **Fragments that don't connect.** "One app. One tap." reads choppy. "One app, one tap" flows.
- **Missing context.** "5 minutes after" leaves you asking after what.
- **Stacked short fragments.** "No notes. No typing. I just listen." reads like a robot.

## After generating

Walk the user through the read-aloud test on each variant. Offer to rewrite any that stumble. Then offer to:

1. Generate the same concept across more audience segments
2. Run the script through the curation checklist (invoke `creative-curator`)
3. Build the visual prompts for this concept (invoke `visual-director`)
