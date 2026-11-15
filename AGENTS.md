# Agent Rules (skills)

This workspace uses the skills defined in `skills`:

- **UI & Design System (`skills/ui-craft/SKILL.md`):** Follow the 3P framework (*Purpose, Principles, Personality*) and the 60-30-10 color budget. Use matte surfaces without multi-color `radial-gradient` aurora glows, cohesive OKLCH/tinted neutrals with soft dark-mode lightness (`22%` to `24%`), fluid `clamp()` typography capped at `62ch` line width, restrained radii (`6px` to `14px`), and viewport-aware media loading.
- **Copy & Tone (`skills/natural-copy/SKILL.md`):** Write direct, human prose without em dashes (`—` or `–`), negative parallelisms ("not X, but Y"), or marketing fluff. For Norwegian (`nb`) copy and voice scripts, use natural spoken Bokmål and retain standard English developer terms (`frontend`, `backend`, `fullstack`, `remote`, `soft delete`, `edge cases`, `state`) instead of inventing literal compound translations.
- **Architecture & Code (`skills/lean-architecture/SKILL.md`):** Lock constraints on paper and in `AGENTS.md` before coding, work in *Spike and Stabilize* cycles, make small frequent commits (never mixing refactoring and behavior changes in the same commit), keep a single source of truth for shared data, prefer deletion over addition, and document silent production gotchas in `README.md`.
