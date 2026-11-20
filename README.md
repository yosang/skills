# skills

Practical `SKILL.md` files and `AGENTS.md` rules for AI assisted software development. Built from real world frontend, backend, and design system work to keep generated code, interfaces, and copy grounded.

1. **[`ui-craft`](./skills/ui-craft/SKILL.md):** Design system and frontend rules grounded in Matt D. Smith's (MDS / [Shift Nudge](https://shiftnudge.com)) 3P framework (*Purpose, Principles, Personality*), the gallery principle (achromatic UI chrome with `#ffffff` product grounds and curated light/dark section rhythm), fluid `clamp()` typography ([Utopia.fyi](https://utopia.fyi)) with `300` to `400` display weights, sharp `2px` to `6px` architectural geometry without card shadows or glass pills, zero blocking transitions or scroll hijacking, and viewport-aware media performance.
2. **[`natural-copy`](./skills/natural-copy/SKILL.md):** Rules for direct, human UI copy, case studies, documentation, and voice/chat scripts in both English and Norwegian (`nb`), stripping LLM filler, em dashes, middot separators, `Label: Description.` bullet templates, mid-sentence colons, and stiff literal translations of technical terms.
3. **[`lean-architecture`](./skills/lean-architecture/SKILL.md):** Workflow and code rules for planning constraints before code, building in Dan North's [*Spike and Stabilize*](https://dannorth.net/blog/on-craftsmanship/) cycles, keeping a single source of truth for data, preferring deletion over addition, and documenting silent production gotchas.

## Repository Structure

```text
skills/
├── AGENTS.md
├── LICENSE
├── README.md
└── skills/
    ├── lean-architecture/
    │   └── SKILL.md
    ├── natural-copy/
    │   └── SKILL.md
    └── ui-craft/
        └── SKILL.md
```

## Usage

Copy the `skills/` folders into `.agents/skills/` (compatible with tools supporting the Agent Skills standard such as Claude Code, Cursor, Antigravity, and Gemini CLI), or drop [`AGENTS.md`](./AGENTS.md) directly into the root of your repository.

## Extending and Contributing

This repository is meant to evolve as new patterns and failure modes show up in real projects.

### 1. Updating an Existing Skill

When an LLM repeats a mistake in a project, add a concrete rule to the relevant skill:

- **UI or CSS defaults:** Add the anti-pattern and its exact token replacement to [`skills/ui-craft/SKILL.md`](./skills/ui-craft/SKILL.md).
- **Copy or translation habits:** Add the phrase or literal translation to the replacement table in [`skills/natural-copy/SKILL.md`](./skills/natural-copy/SKILL.md).
- **Architecture, testing, or deployment gotchas:** Add the rule and a brief example to [`skills/lean-architecture/SKILL.md`](./skills/lean-architecture/SKILL.md).

### 2. Adding a New Skill

Create a new folder under `skills/<skill-name>/SKILL.md` with YAML frontmatter:

```markdown
---
name: <skill-name>
description: "Short description of what the skill enforces and when the agent should load it."
---

# <skill-name>

2 to 3 sentences explaining the exact problem this skill solves.

## 1. <First Core Rule>

- Concrete instruction showing what to avoid and what to do instead.
```

### 3. Guidelines for Skills

To keep context usage low and signal high:

1. **Only rules that change model behavior:** Skip generic textbook advice the model already follows by default. Every rule should counter a specific default habit.
2. **Concrete tokens over vague adjectives:** Specify exact ratios, CSS `clamp()` formulas, hex/OKLCH values, or before/after phrasing rather than asking for "clean design" or "good writing".
3. **Keep skill files under 100 lines:** If a skill needs longer reference tables or helper scripts, place them in `references/` or `scripts/` inside that skill's folder.
4. **Update the index:** When adding a new skill, list it in [`AGENTS.md`](./AGENTS.md) and at the top of this README.

## References & Credits

- **The 3P Framework (*Purpose, Principles, Personality*):** Matt D. Smith (MDS), creator of [Shift Nudge](https://shiftnudge.com) ([The 3 P's of UI Design](https://www.youtube.com/watch?v=V-2inD5HEZ4)).
- **Hierarchy of User Needs (*Functional, Reliable, Usable, Delightful*):** Aarron Walter, *Designing for Emotion* (A Book Apart).
- **Fluid Responsive Type & Space (`clamp()`):** Trys Mudford and James Gilyead, [Utopia.fyi](https://utopia.fyi).
- **Spike and Stabilize:** Dan North, [On Craftsmanship](https://dannorth.net/blog/on-craftsmanship/).

## License

MIT © Yosmel Chiang
