# Runway Gen-4 Mockup Animator

Animates a static phone mockup into a five-second clip. Useful when you have a strong static product shot and need to give it motion for video placements. The phone bezel and background stay static; only the screen content slides.

## How to use

Upload your static 9:16 phone mockup as the input image to Runway Gen-4. Paste the prompt. The static must show the first screen state; Runway will interpolate motion to the next two states based on the prompt.

## The prompt

```
Input: the attached static 9:16 phone mockup image. Animate as a five-second clip. The phone holds steady in frame for the first half second. Then the phone screen content slides smoothly from screen one to screen two to screen three, each screen visible for roughly 1.2 seconds, with a soft horizontal swipe transition between them. While the screens slide, the camera does a subtle slow push-in on the phone, roughly 8 percent zoom over the full duration. Keep the phone bezel and background plate completely static. Lighting should match the source image. Motion should feel intentional and product-demo clean, not floaty or AI-drifty. Do NOT add: any text overlays, any hands holding the phone, any background motion, any color shift, any reflections that were not in the source.
```

## Tips

- The cleaner your source image, the cleaner the motion. Prepare the static in Figma with the three screen states baked into adjacent frames if possible.
- If Runway introduces unwanted motion (background drift, color flicker), regenerate with sharper "do NOT" constraints in the prompt.
- For phone-screen animations specifically, screen recording the actual app and compositing in After Effects often beats a Runway animation. Use AI for what cannot be screen-recorded.
