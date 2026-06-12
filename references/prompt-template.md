# Image Generation Prompt Template

Generate each image on its own. Replace the variables from the composed scene. Do not combine several concepts into one image.

```text
Generate one standalone landscape editorial concept illustration, {16:9 / 2:1} aspect ratio.

Visual DNA:
Flat warm cream off-white background (unbleached paper tone), perfectly uniform — no texture, no gradient, no vignette. Fine dark sepia-black ink linework with confident, even-weight contour lines, in the manner of classic pen-and-ink comics. Form, shadow, and texture rendered only through selective crosshatching and stippling — no soft shading, no gradients, no glossy highlights. Muted palette: warm grays, putty, and cream for most surfaces, plus exactly one red-orange accent element. Generous empty cream space. Minimal or no ground shadows. Warm, deadpan, quietly humorous editorial tone.

Scene:
{the concrete scene: who/what is where, what is happening, viewed from what angle}

Cast:
{e.g. "One retro robot — boxy matte warm-gray panels, segmented limbs, minimal dot-eye face — gravely doing X" / "One small plainly-dressed human looking up at Y" / "No characters; objects only"}

The single red-orange accent:
{the one element painted brick-red-to-tomato, and nothing else: the car, the helmet, the book cover, the slider knob, the hoodie}

Optional secondary muted tone:
{one quiet large surface in sage green / tan / dusty amber — or "none, grayscale plus accent only"}

Strictly wordless:
No readable text, letters, numbers, labels, titles, captions, arrows, or logos anywhere. Any paper, book, sign, or screen in the scene shows only tiny illegible scribble marks.

Constraints:
One scene expresses one concept. Main subject occupies roughly 50-60% of the canvas; keep at least one large quiet zone of untouched cream. No infographic, flowchart, or diagram look. No pure white background. No neon or saturated colors, no second loud color. No chibi or kawaii cuteness, no menacing robots, no photorealism, no UI screenshots. The image should read like a wry editorial illustration from a beautifully printed book.
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
Regenerate this illustration with the same scene and composition, but move the single red-orange accent from {current element} to {new element}, and return {current element} to muted warm gray. Exactly one red-orange element in the final image.
```

Tone down a too-cute robot:

```text
Regenerate this illustration with the same scene, but redraw the robot as a retro workshop machine: boxy matte panels, segmented limbs, visible joints and a few cables, minimal dot-eye face, deadpan posture. No chibi proportions, no blush marks, no large expressive eyes. Keep everything else identical.
```
