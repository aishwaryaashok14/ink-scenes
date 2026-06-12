---
name: ink-scenes
description: Turn a technical concept into one wordless, editorial scene illustration — warm cream background, fine ink linework with crosshatch detail, muted palette with one red-orange accent, friendly retro robots standing in for software/AI. Use when the user wants an ink-scene illustration, a wordless visual metaphor for a technical term or idea, an editorial header image for a post, or says "ink scene" / "robot illustration for X" / "draw this concept as a scene".
---

# Ink Scenes

## Core idea

Turn one technical concept into one landscape, **wordless** scene illustration. The goal is the feel of a thoughtful editorial illustration in a beautifully printed book: an everyday physical scene — a dinner table, a drive-through, a desk, a street — that *is* the concept, drawn in fine ink on warm cream paper, so the reader gets it in a beat or two without a single readable word.

The recurring cast is **robots and small ordinary humans**. Robots play software, AI, servers, and machines — friendly, retro, matte, a little tired, never menacing. Humans play users — small, plainly dressed, often dwarfed by what they're dealing with. Many images need no characters at all: two objects side by side can carry the whole metaphor (a full holiday dinner table next to a blender of beige purée *is* compaction).

Input is a **concept**, not an article. The skill's job is to invent the everyday metaphor, stage it as one quiet scene, and draw it well.

## The contract: compose first, then draw

For each concept, **think briefly out loud, then generate one image**. Before calling the image model, state:

- **Metaphor** — the everyday scene that stands in for the concept.
- **Cast** — robot(s), human(s), or objects only, and what each is doing.
- **The accent** — the dominant red-orange carrier (plus any tiny echoes), and why the eye should land on it.
- **Composition** — single scene or two-panel before/after; where the weight sits; where the quiet cream space is.

Then generate **one** image. One concept → one composed image. Do not fan out into variations unless the user asks. If the user gives several concepts, make one image each.

## Read these references as needed

Pull in only what the task needs; do not load everything at once:

- `references/style-dna.md` — the visual DNA: cream ground, ink line, crosshatch, the one-accent rule, hard nos.
- `references/cast-and-props.md` — how the robots and humans look and behave, and the everyday-object prop pool.
- `references/composition-patterns.md` — scene structures and how to invent a fresh metaphor every time.
- `references/prompt-template.md` — the fill-in-the-blanks single-image generation prompt.
- `references/qa-checklist.md` — post-generation checks and iteration moves.
- `assets/examples/` — saved reference images in this style (personal style reference only; do not republish).

## Workflow

### 1. Read the concept

Decide what *shape* the concept has: a transformation (input becomes output), a contrast (before/after, with/without), a relationship (one thing serving another), a state (overload, idle, waiting), or a hidden mechanism (what's really going on inside). That shape picks the composition. Illustrate the single concept in front of you — do not stuff an article's worth of nuance into one scene.

### 2. Compose (think briefly)

State the metaphor, cast, accent, and composition (see "The contract" above). A few lines — enough for the user to catch a wrong take in one second.

### 3. Generate one image

If the user clearly asks to generate, do not stop for confirmation — use the built-in image tool with the prompt template. Every prompt must include:

- landscape concept illustration (default 16:9; 2:1 for wide quiet scenes)
- flat warm cream / off-white background, no texture, no gradient
- fine dark sepia-black ink linework, confident and clean, with selective crosshatching and stippling for form and texture
- muted palette: warm grays and cream, quiet earth tones (sage, tan, dusty amber) where the scene needs them, plus one red-orange accent hue with a single dominant carrier
- **no readable text anywhere** — any paper, screen, or book in the scene shows only illegible scribble marks
- generous negative space and minimal ground shadows
- no infographic look, no labels or arrows, no neon or saturated color, no pure white background, no chibi cuteness, no menace

Invent a fresh metaphor for every concept. Do not reuse a metaphor from a previous image unless the user explicitly asks to reuse or remix one.

### 4. Check and iterate

Run `references/qa-checklist.md`. Regenerate or do a local edit if:

- readable text or labels crept in
- the background drifted to pure white, or gained texture/gradient
- a second saturated color competes with the red-orange accent
- it reads as an infographic, diagram, or slide instead of a scene
- the robots turned cute-chibi or sinister
- the canvas is too full — no quiet zone left
- the metaphor needs a caption to land

### 5. Save and report

If working inside a project workspace, copy the final image to:

```text
assets/<concept-slug>-illustrations/
```

Otherwise, save to the default local library (kept out of git):

```text
~/ink-scenes/output/<concept-slug>/
```

Name in order:

```text
01-concept-name.png
02-concept-name.png
```

Keep the original generated file. Do not overwrite existing assets unless the user asks to replace them.

## Output register

Keep the pre-generation "compose" note short and concrete. After generating, report:

- how many images were made
- what each one is
- the save path

Let the image do the talking; do not lecture about style theory.
