# Production Checklist

Run this DURING AI generation. Production is the AI's job; the human's job in this phase is to supervise: keep the strategy layer constant, vary only the production layer, and stop when you have enough comparable variants.

## The checklist

- [ ] **Generating across the eight axes simultaneously, not one at a time.** Hook copy, background color, duration, music, VO type, scene order, transition style, visual hook treatment.

- [ ] **Scripts built on Setup / Shift / Proof / Payoff, not training-data defaults.** No autopilot PAS, BAB, AIDA. Each beat constrained by the bet and the craft.

- [ ] **Strategy layer is constant across variants.** Same angle, same hook layer assignments, same format. Vary the production layer only. This is what makes test results readable.

- [ ] **Each prompt has a "do NOT include" section.** Every visual prompt, every script prompt. The forbidden list is the brief.

- [ ] **Aspect ratio specified in every visual prompt.** 4:5 for Meta feed, 9:16 for Reels and TikTok, 1:1 for square. The model defaults to square or 16:9 if you don't specify.

- [ ] **Generating in the right tool for the job.** Midjourney for mood, Gemini for accuracy, Kling or Gemini Omni Flash for motion, Runway for animating stills, ElevenLabs for voice, Claude for rule-following, ChatGPT for speed.

- [ ] **Stopping at the right ceiling.** Twelve to twenty variants per concept across three formats is usually right. Beyond that, you're diluting learning.

## Three cohorts to run in parallel

For a concept entering test, run three cohorts simultaneously:

1. **Hook copy cohort.** Same visual, same format, same script. Only the text overlay or first VO line varies.
2. **Visual hook cohort.** Same hook copy, same format, same script. Only the visual treatment varies.
3. **Format cohort.** Same hook copy, same visual treatment. Different format (Discovery vs. Transformation vs. Wall of Text).

Hold the strategy layer constant within a cohort. Vary the production layer only.

## Failure modes to catch

- Generating one variant at a time instead of in parallel
- Letting the angle drift across variants in the same cohort
- Asking the AI to do too many things in one prompt (hero shot plus three product features plus on-screen text plus a logo)
- Defaulting to "cinematic" or "photorealistic" without specifying style
- Skipping the aspect ratio
- Letting the AI generate faces when faceless would test stronger
- Using AI footage where stock or app screen recordings would be cheaper and stronger
- Not specifying duration or pacing for video

When any of these fire, the cost is downstream: variants that look fine but produce noise instead of signal.
