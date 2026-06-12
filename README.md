# Ink Scenes

> Some ideas are better drawn than defined.

[![License: MIT](https://img.shields.io/badge/License-MIT-black.svg)](LICENSE)
[![Claude Code skill](https://img.shields.io/badge/Claude_Code-skill-c0392b)](#bring-it-home)
[![OpenAI Codex skill](https://img.shields.io/badge/OpenAI_Codex-skill-c0392b)](#bring-it-home)
[![GitHub stars](https://img.shields.io/github/stars/aishwaryaashok14/ink-scenes?style=social)](https://github.com/aishwaryaashok14/ink-scenes/stargazers)

Explaining a server to your grandmother doesn't take a diagram.
It takes her kitchen.

**Ink Scenes** is an agent skill that takes a technical concept — *compaction*, *queue*, *technical debt* — and draws the everyday scene that already contains it. A full dinner table beside a blender of beige purée. A drawer that no longer closes. The drawing carries the whole idea, so the words can stay home: no labels, no arrows, no captions. If the image needs one, the image failed.

Made by [Aishwarya Ashok](https://x.com/aishashok14) · [LinkedIn](https://www.linkedin.com/in/aishwarya-ashok/)

```text
Use $ink-scenes to draw a wordless concept illustration for:
"compaction"
```

## The world it draws

Every image lives in the same small, patient world.

The paper is warm cream — `#F0E8DB`, the color of a page that has waited a while for its drawing. The line is ink, near-black with a brown memory of the pen — `#1C120B` — confident and even, the kind of line you earn by drawing the same kettle a hundred times. Shadows aren't painted; they're *hatched*, stroke by stroke, the old way.

Almost everything wears quiet colors. Putty, warm gray, a sage so hushed it's nearly gray, the dusty amber of bread and old paper. And then — one red thing. Brick to tomato, `#8B3C35` to `#DF4E31`. One per image. It sits exactly where the idea pivots, and your eye goes to it the way it goes to the one lit window on a dark street.

The software is played by robots — retro, matte, a little tired, taking their mundane jobs completely seriously. A robot in a chef's hat is not a joke about robots; it's a portrait of a process. The users are played by small, plainly drawn people, often standing in front of something much larger than themselves. That asymmetry is most of what needs saying.

And everywhere: room. Big quiet fields of untouched cream. The scene takes only the space it needs, the way a good explanation does.

## How it thinks

The skill composes before it draws, out loud, where you can stop it:

1. **The metaphor** — which everyday scene already *is* this concept
2. **The cast** — robots, humans, or just objects on a table
3. **The red thing** — what the eye should land on, and why
4. **The room** — where the weight sits, where the quiet survives

Then one image. Not four variants, not a contact sheet. One concept, one scene, composed like a sentence with no spare words — and checked afterward against a hard list: did the background drift white, did a stray label sneak in, did the robot get cute. Failures get redrawn.

## Say it like this

Draw one concept:

```text
Use $ink-scenes to draw a wordless concept illustration for:

prompt caching

Everyday scene metaphor, cream background, one red-orange accent, no words.
```

Draw a few — each gets its own scene, never a collage:

```text
Use $ink-scenes to draw one image each for: queue, webhook, cache.
```

Change the signature color — the discipline stays, the hue is yours:

```text
Use $ink-scenes to draw "vector database", but swap the red-orange accent
for deep teal — same restraint, one dominant carrier.
```

Mend an image:

```text
Use $ink-scenes to edit this image: the background drifted to pure white —
bring it back to flat warm cream, keep everything else identical.
```

More in [examples/prompts.md](examples/prompts.md).

## What it refuses

This is a skill with manners, which is to say: a long list of nos.

No infographics. No flowcharts wearing a costume. No arrows with opinions. No pure white. No gradients, no gloss, no neon. No text — papers and screens in the scene carry only a quiet scribble that reads as writing from across the room and says nothing up close. No kawaii robots, no menacing ones. No second loud color, ever.

Restraint is the style. Everything the images don't do is why they work.

## Bring it home

```bash
git clone https://github.com/aishwaryaashok14/ink-scenes.git
cd ink-scenes
```

**Claude Code**

```bash
mkdir -p "$HOME/.claude/skills"
cp -R ./ink-scenes "$HOME/.claude/skills/"
```

**OpenAI Codex**

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ink-scenes "${CODEX_HOME:-$HOME/.codex}/skills/"
```

Prefer your clone to stay the single source of truth? Symlink instead:

```bash
ln -s "$(pwd)/ink-scenes" ~/.claude/skills/ink-scenes
```

Then ask for any concept, wordlessly drawn. Images land in `output/<concept>/`, or your project's `assets/` folder when you're working inside one.

## Gallery

Coming soon — the first drawings are on their way. Run any prompt from [examples/prompts.md](examples/prompts.md) and send your favorites to `examples/images/` via PR.

## The bones

```text
.
├── README.md            ← you are here
├── LICENSE
├── examples/
│   ├── images/          ← the gallery grows here
│   └── prompts.md       ← copy-paste starting points
└── ink-scenes/          ← the installable skill
    ├── SKILL.md            the contract: compose first, draw once
    ├── agents/openai.yaml
    └── references/
        ├── style-dna.md            the cream, the ink, the one red thing
        ├── cast-and-props.md       robots, small humans, flea-market objects
        ├── composition-patterns.md six ways to stage a concept
        ├── prompt-template.md      the generation prompt, measured hexes included
        └── qa-checklist.md         what gets an image redrawn
```

## License

MIT. See [LICENSE](LICENSE).

Take the style somewhere good — and leave the canvas quieter than you found it.
