---
name: visual-director
description: Build production-ready prompts for AI image, video, and audio tools. Covers Midjourney v7 (stylized stills), Gemini 3 Pro Image (photorealistic scenes), Sora 2 (short generative video), Runway Gen-4 (image-to-video, motion control), and ElevenLabs (voice cloning, TTS with emotional direction). Enforces the negative-space rule. Use when briefing AI tools for ad creative production.
---

# Visual Director

Build production-grade prompts for AI image, video, and audio generation.

## When invoked

Ask:

1. **What format do you need?** (still image, short video, animated mockup, voiceover)
2. **What's the visual concept?** (one-line description of the scene or motion)
3. **What vertical / category?** (sleep app, finance app, meditation, etc.)
4. **Aspect ratio?** (9:16 for Reels and TikTok, 4:5 for Meta feed, 1:1 for square)
5. **Negative space?** (what should NOT appear: faces, hands, stock-photo styling, specific cliches)

Then route to the right tool and prompt template:

| Use case | Tool | Prompt file |
|---|---|---|
| Stylized destruction-theme still | Midjourney v7 | `prompts/midjourney-destruction-hook.md` |
| Photorealistic cluttered/pain-point shot | Gemini 3 Pro Image | `prompts/gemini-cluttered-desk.md` |
| Short generative transformation video | Sora 2 | `prompts/sora-transformation-clip.md` |
| Animate a static mockup | Runway Gen-4 | `prompts/runway-mockup-animator.md` |
| Voiceover with emotional direction | ElevenLabs | `prompts/elevenlabs-vo-direction.md` |

## The negative-space rule

Every prompt must include a "do NOT include" section. The forbidden list is the brief.

Examples that should appear in almost every prompt:

- no faces, no hands (unless critical and willing to inpaint later)
- no actor looking shocked or surprised
- no generic stock-photo backgrounds
- no stock-music-sounding tracks
- no invented statistics
- no on-screen text the model will mangle
- no logos other than the one you provide
- no AI artifact tells (extra fingers, melted text)

The model's defaults are everyone else's defaults. The forbidden list is what makes the output specific to your brand.

## Tool selection cheat sheet

- Midjourney for mood
- Gemini for accuracy
- Sora for motion
- Runway for animating stills
- ElevenLabs for voice
- Pika for stylized animation
- Claude for rule-following at length
- ChatGPT for speed

## Edit vs. regenerate

After generation, ask: is the seed wrong, or is it 90% right with one fixable element?

- **Regenerate** if subject, scene, tone, or composition is fundamentally wrong.
- **Edit** if 90% is right (overlay zone, color, dollar value, hand position, distracting clutter). Use inpainting in Sora/DALL-E, color correction in Photoshop/Figma, compositing in After Effects/CapCut.

Most teams over-regenerate. Edit until you can't, then regenerate.

## After generating

Offer to:
1. Generate variants of the same prompt with different style references
2. Build the script that pairs with this visual (invoke `script-maker`)
3. Run the variant through the curation checklist (invoke `creative-curator`)
