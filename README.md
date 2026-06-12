# Ink Scenes

An agent skill that turns a technical concept into one **wordless, editorial scene illustration** — fine ink linework on warm cream paper, a muted palette with a single red-orange accent, and friendly retro robots standing in for software and AI.

Give it a concept ("prompt caching", "webhook", "technical debt") and it invents an everyday physical metaphor — a dinner table, a drive-through, a cluttered desk — composes the scene out loud so you can veto a bad take, then generates exactly one image. No labels, no captions, no diagram furniture: if the metaphor needs a word to land, it failed.

## Style at a glance

- Landscape (16:9 or 2:1), flat warm cream background — never pure white, never textured
- Fine sepia-black ink contour lines; form and shadow from crosshatching and stippling only
- Warm grays and cream everywhere, plus **exactly one** red-orange accent on the story's pivot
- Completely wordless — any in-scene paper or screen shows only illegible scribble
- Retro, matte, deadpan robots play the software; small plainly-dressed humans play the users
- One concept, one scene, one image — with a large quiet zone always left untouched

## Install

Works with any agent runtime that reads `SKILL.md`-format skills.

**Claude Code:**

```sh
ln -s "$(pwd)" ~/.claude/skills/ink-scenes
```

**Codex CLI:**

```sh
ln -s "$(pwd)" ~/.codex/skills/ink-scenes
```

(Or `cp -R` instead of `ln -s` if you prefer a frozen copy.)

## Use

- Claude Code: `/ink-scenes prompt caching`
- Codex: `$ink-scenes prompt caching` — or just ask for "a wordless concept illustration for X"; implicit invocation is enabled via `agents/openai.yaml`

The skill composes first (metaphor, cast, accent, composition), generates one image, then self-checks against `references/qa-checklist.md` and iterates if the style drifted.

## Layout

```
SKILL.md                          entry point: contract + workflow
references/
  style-dna.md                    the visual rules and hard nos
  cast-and-props.md               robots, humans, and the prop pool
  composition-patterns.md         scene structures + metaphor invention
  prompt-template.md              generation + edit prompts
  qa-checklist.md                 pass criteria and iteration moves
agents/openai.yaml                Codex interface metadata
assets/examples/                  local style references (not tracked in git)
output/                           generated images land here (not tracked in git)
```
