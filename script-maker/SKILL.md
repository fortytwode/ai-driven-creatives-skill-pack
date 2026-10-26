---
name: script-maker
description: Generate direct-response ad scripts using the Setup / Shift / Proof / Payoff structure, constrained by the concept's bet and the body craft. Avoids autopilot PAS, BAB, AIDA templates. Enforces 45-65 word length, conversational first-person tone, and the read-aloud test. Use when drafting video ad scripts for subscription apps.
---

# Script Maker

Generate ad scripts using RocketShip HQ's Setup / Shift / Proof / Payoff structure. The structure is the skeleton; the bet (who this is for, what it is against) and the body craft (open on the pain, one concrete situation, a visible mechanism) are what make it perform.

## When invoked

Ask:

1. **App and category?**
2. **User problem?**
3. **Concept angle for this script?** (one-line emotional hook or contrarian framing)
4. **Audience?** (specific segment, e.g., "ESL professionals", "parents of neurodivergent kids", "marathon runners with insomnia")
5. **Mode?** (one of: 3 variants from one brief, rewrite a flat AI-generated script, 3 audience-segment variants of the same concept)

Then load the corresponding prompt:

| Mode | Prompt file |
|---|---|
| 3 variants from one brief | `prompts/script-maker.md` |
| Rewrite a flat AI-generated script | `prompts/flat-script-rewriter.md` |
| 3 audience segment variants | `prompts/audience-segment-maker.md` |

For verbal hooks (first VO line, separate from a full script), invoke the `hook-maker` skill instead.

## The structure: Setup / Shift / Proof / Payoff

Four beats, in order:

1. **Setup** (the opening): the situation, problem, or discovery moment that opens the ad
2. **Shift** (the change): what changes once the product or method appears
3. **Proof** (the evidence): a concrete screen, behavior, or result that makes the promise believable
4. **Payoff** (the close): what the viewer should remember or do next

Example for a productivity app that records meetings:

- Setup: "I used to spend 20 minutes after every meeting trying to remember what was said."
- Shift: "Now I just hit record on my phone and slip it in my pocket."
- Proof: "It transcribes everything and gives me a perfect summary."
- Payoff: "My coworkers think I have a photographic memory. I don't correct them."

It is not a law. Name your beats, make each one set up the next, and use a different shape if it serves the ad better. The discipline is in not skipping a beat.

## The bars every script must clear

- **Continue the hook.** Pick the story up after the hook lands; don't restate it.
- **Move through a real change.** A belief, a behavior, a discovery, a comparison, or a result.
- **Go deep on ONE concrete situation.** One specific lived detail beats three named in passing.
- **Make the mechanism visible.** Show why the product changes the outcome, not just that it does.
- **Sound like a person with a point of view.** Not a brand, not a stack of clipped fragments.
- **Pay off exactly the loop the hook opened.**
- **Proof proportionate to the claim.** A big claim needs hard proof.
- **Open on the pain, close on the gain.**

Then three passes, in order: sequence, intensify, compress.

## Hard rules

- 45 to 65 words per script. Never exceed 70.
- Conversational, first-person.
- Flowing sentences. No stacked fragments.
- No sentence starts with the product name.
- Don't autocomplete a familiar template (PAS, AIDA, BAB) on autopilot. Build on the four beats.
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
