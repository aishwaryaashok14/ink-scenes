# Image Generation Prompt Template

Generate each image on its own. Replace the variables from the composed scene. Do not combine several concepts into one image.

```text
Generate one standalone landscape editorial concept illustration, {16:9 / 2:1} aspect ratio.

Visual DNA:
Flat warm cream off-white background (unbleached paper tone), perfectly uniform — no texture, no gradient, no vignette. Fine dark sepia-black ink linework with confident, even-weight contour lines, in the manner of classic pen-and-ink comics. Form, shadow, and texture rendered only through selective crosshatching and stippling — no soft shading, no gradients, no glossy highlights. Muted palette: warm grays, putty, and cream for most surfaces, quiet low-saturation earth tones (sage, tan, dusty amber) where the scene needs them, plus one red-orange accent hue with a single dominant carrier. Generous empty cream space. Minimal or no ground shadows. Warm, deadpan, quietly humorous editorial tone.

Scene:
{the concrete scene: who/what is where, what is happening, viewed from what angle}

Cast:
{e.g. "One retro robot — boxy matte warm-gray panels, segmented limbs, minimal dot-eye face — gravely doing X" / "One small plainly-dressed human looking up at Y" / "No characters; objects only"}

The red-orange accent:
{the one dominant carrier painted brick-red-to-tomato — the car, the protagonist robot's helmet and torso, the blender base, the hoodie — plus at most a couple of tiny echoes of the same hue, e.g. "a thin pinstripe on the tablecloth" / "a small knob" / "none"}

Quiet earth tones:
{the hushed low-saturation tones the scene needs, e.g. "sage green bin, tan bread, dusty-amber turkey" — or "none, grayscale plus accent only"; every earth tone clearly quieter than the accent}

Strictly wordless:
No readable words, labels, titles, captions, arrows, or logos anywhere. Any paper, book, sign, or screen in the scene shows only tiny illegible scribble marks. {If counting is the point: "Tiny plain numerals are allowed on {the tickets/the dial} only." — otherwise: "No numbers either."}

Constraints:
One scene expresses one concept. Main subject occupies roughly 50-60% of the canvas; keep at least one large quiet zone of untouched cream. No infographic, flowchart, or diagram look. No pure white background. No neon or saturated colors, no second loud color. No kawaii faces (no blush marks or giant anime eyes — small rounded deadpan robots are fine), no menacing robots, no photorealism, no UI screenshots. The image should read like a wry editorial illustration from a beautifully printed book.
```

## Image edit prompts

Remove stray text:

```text
Edit the provided image. Remove the readable text "{text}" and replace that area with {matching cream background / illegible scribble marks consistent with the surrounding drawing}. Preserve everything else exactly: linework, crosshatching, the single red-orange accent, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

Fix a drifted background:

```text
Regenerate this illustration unchanged except for the background: make it a single flat warm cream off-white tone with no texture, gradient, or vignette. Keep the ink linework, crosshatching, muted palette, single red-orange accent, and composition identical.
```

Move the accent:

```text
Regenerate this illustration with the same scene and composition, but move the dominant red-orange accent from {current element} to {new element}, and return {current element} to muted warm gray. One dominant red-orange carrier in the final image.
```

Tone down a too-cute robot:

```text
Regenerate this illustration with the same scene, but redraw the robot as a retro workshop machine: boxy matte panels, segmented limbs, visible joints and a few cables, minimal dot-eye face, deadpan posture. No chibi proportions, no blush marks, no large expressive eyes. Keep everything else identical.
```
