# Ink Scenes

> Turn any technical concept into one wordless ink-on-cream scene — no labels, no arrows, just a metaphor that lands in two seconds.

[![License: MIT](https://img.shields.io/badge/License-MIT-black.svg)](LICENSE)
[![Claude Code skill](https://img.shields.io/badge/Claude_Code-skill-c0392b)](#install)
[![OpenAI Codex skill](https://img.shields.io/badge/OpenAI_Codex-skill-c0392b)](#install)
[![GitHub stars](https://img.shields.io/github/stars/aishwaryaashok14/ink-scenes?style=social)](https://github.com/aishwaryaashok14/ink-scenes/stargazers)

**Ink Scenes** is an AI-agent skill for making editorial concept illustrations the way a comics artist with a dip pen would explain a server to their grandmother: by drawing her kitchen. Give it a technical term — *queue*, *cache*, *compaction* — and it invents an everyday physical scene that **is** the concept, composes it out loud so you can veto a bad take, and generates exactly one image.

**Built by Aishwarya Ashok** - [X](https://x.com/aishashok14) · [LinkedIn](https://www.linkedin.com/in/aishwarya-ashok/)

```text
Use $ink-scenes to draw a wordless concept illustration for:
"compaction"
```

## The look

- **Warm cream paper** — never pure white, never textured
- **Fine sepia-black ink** — clean contour lines, with crosshatching and stippling doing all the shading
- **One red-orange flare** — a single dominant accent carrier per image; when there's a crowd, the red one is the protagonist
- **Quiet earth tones** — sage, tan, dusty amber, all hushed below the accent
- **Retro robots as the cast** — software and AI played by matte, deadpan workshop droids; users played by small ordinary humans
- **Completely wordless** — papers and screens show only illegible scribble; if the metaphor needs a caption, it failed

## Why wordless?

Most "concept illustrations" are diagrams wearing a costume — boxes, arrows, labels. This skill bans all of it. A queue is a line of small robots holding numbered tickets at a drive-through window. A job is one order ticket pulled off the rail. A cache is the chef's walk-in fridge. When the metaphor is right, the word becomes unnecessary — and that's the test the skill holds itself to.

## Gallery

Coming soon — run any prompt from [examples/prompts.md](examples/prompts.md) and the skill will compose, generate, and QA one image per concept. Add your favorites to `examples/images/` via PR.

## Install

Clone the repo:

```bash
git clone https://github.com/aishwaryaashok14/ink-scenes.git
cd ink-scenes
```

### Claude Code

```bash
mkdir -p "$HOME/.claude/skills"
cp -R ./ink-scenes "$HOME/.claude/skills/"
```

Then invoke it:

```text
Use $ink-scenes to draw a wordless concept illustration for:
"technical debt"
```

### OpenAI Codex

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ink-scenes "${CODEX_HOME:-$HOME/.codex}/skills/"
```

Then invoke it:

```text
Use $ink-scenes to draw a wordless concept illustration for:
"a webhook"
```

(Symlink instead of copy — `ln -s "$(pwd)/ink-scenes" ~/.claude/skills/ink-scenes` — if you want your clone to stay the single source of truth.)

## What makes it different

- **Wordless by contract.** No labels, no titles, no annotated arrows — the metaphor has to carry everything.
- **Compose first, draw second.** The skill states the metaphor, cast, accent placement, and layout before generating, so you can kill a weak take before it costs an image.
- **One accent, one protagonist.** A single red-orange hue with one dominant carrier per image; in a crowd of gray robots, the red one is the process you're following.
- **Series-aware.** Related concepts can share one coherent world — the ticket rail is the queue, one ticket is a job, the walk-in fridge is the cache — so a reader who got one image gets the next faster.
- **Self-checking.** Every image is run against a QA checklist (background drift, stray text, accent dilution, kawaii drift) and regenerated or locally edited on failure.

## How to use

### Draw one concept

```text
Use $ink-scenes to draw a wordless concept illustration for:

prompt caching

Everyday scene metaphor, cream background, one red-orange accent, no words.
```

### Draw a series in one world

```text
Use $ink-scenes to draw one image each for: queue, job, cache.

Keep all three in the same restaurant world so the metaphors compound.
One composed image per concept, not a collage.
```

### Swap the signature color

```text
Use $ink-scenes to draw "vector database", but swap the red-orange accent
for deep teal — same restraint, one dominant carrier.
```

### Edit an image

```text
Use $ink-scenes to edit this image: the background drifted to pure white —
bring it back to flat warm cream, keep everything else identical.
```

## What it produces

By default:

- one landscape (16:9 or 2:1) scene illustration per concept
- a short compose note (metaphor / cast / accent / layout) before each image
- a final PNG saved to `output/<concept-slug>/` (or your project's `assets/` folder)

By default not:

- diagrams, flowcharts, or labeled infographics
- slides, posters, or text-heavy explainers
- variations or collages (one concept, one image — unless you ask)

## How it works

1. Read the concept and identify its shape: transformation, contrast, relationship, state, or hidden mechanism.
2. Compose the scene: everyday metaphor, cast (robots / humans / objects only), accent carrier, layout.
3. Generate one image with the image model using the prompt template.
4. Check against the QA list: cream background, ink-and-hatch rendering, one dominant accent, zero readable words, a surviving quiet zone.
5. Save the PNG and report.

## Repo structure

```text
.
├── README.md
├── LICENSE
├── examples/
│   ├── images/
│   └── prompts.md
└── ink-scenes/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    └── references/
        ├── style-dna.md
        ├── cast-and-props.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

The installable agent skill is the `ink-scenes/` subdirectory. The root README, examples, and license are GitHub-facing docs.

## Notes

- The wordless rule is strict on *words*; tiny numerals are allowed when counting is the point (numbered queue tickets, a dial).
- Image models drift: white backgrounds, stray labels, and over-cute robots are the common failure modes — the QA checklist catches all three.
- If a scene only makes sense with a caption, don't fix the rendering — recompose the metaphor.
- One image = one concept. A series shares a world, never a canvas.

## License

MIT License. See [LICENSE](LICENSE).
