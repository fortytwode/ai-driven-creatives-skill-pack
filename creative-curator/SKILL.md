---
name: creative-curator
description: Run a three-phase checklist on any AI creative concept: drafting (before generation), production (during generation), and curation (before shipping). Catches the failure modes that produce sloppy AI or beautiful AI that performs badly. Use before publishing any AI-generated ad creative.
---

# Creative Curator

Walk a concept through three phases of human-in-the-loop checks.

## When invoked

Ask which phase the user is in:

| Phase | When to use | Checklist |
|---|---|---|
| **Drafting** | Before any AI generation | `checklists/drafting-checklist.md` |
| **Production** | During AI generation | `checklists/production-checklist.md` |
| **Curation** | After generation, before shipping | `checklists/curation-checklist.md` |

Run the matching checklist as a structured Q&A. For each item, check whether the concept passes. If not, walk the user through fixing it before moving on. Do not let a concept advance to the next phase until the previous one is clean.

## The principle

The work AI eliminates is production work. The work AI does NOT eliminate is strategy work and curation work. In an AI-driven workflow, those two layers carry more weight than they did in UGC, because the iteration volume is so much higher.

Most teams fail by inverting this. They let the AI default to its training data on the brief (sloppy AI). Or they skip curation because generation was so cheap it felt wasteful to throw outputs away (beautiful AI that dies in market).

The reason humans matter at all three phases: the AI does not know the brand, does not know what's failed in past tests, and does not know which DR principles are non-negotiable. It produces variants. Humans decide which variants represent the brand and which ones don't.

## The eight iteration axes (for the production phase)

When generating variants, vary across these axes. Hold the strategy layer constant within a test cohort; vary the production layer only.

1. **Messaging.** Text overlay variants, hook copy alternatives, comment-style hooks, question hooks.
2. **Background colors.** Overlay color, video background tone, app-screen vignette.
3. **Duration.** 10s, 15s, 20s, 30s for video. Aspect ratio swap for static.
4. **Music.** Uplifting, suspense, ASMR-style, no-music.
5. **Voice over.** TTS, AI-cloned voice, original human, no VO.
6. **Animation.** Transition style, sticker entrance, text emphasis pattern.
7. **Scene order.** Which beat opens, which closes.
8. **Visual hook treatment.** Theme variant, prop substitution, format swap.

## After running

If the concept passes all three checklists, hand off for shipping. If it fails any, route to the appropriate skill:

- Hook layers off → invoke `hook-maker`
- Script flat or off-structure → invoke `script-maker`
- Visual prompts vague or missing negative space → invoke `visual-director`
