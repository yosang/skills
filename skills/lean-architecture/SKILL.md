---
name: lean-architecture
description: "Keep codebases, context windows, and documentation lean and maintainable. Use when planning architecture, writing or refactoring code, writing tests, or documenting repositories."
---

# lean-architecture

Unconstrained AI code generation tends to produce 2x the necessary lines of code, premature abstractions for hypothetical future use cases, duplicated data definitions across files, and generic README boilerplate. This skill keeps architecture flat, context small, and documentation genuinely useful.

## 1. Constraints Before Code & Spike and Stabilize

1. **Paper and `AGENTS.md` First:** Before prompting or writing code, map out the data model and hard platform constraints in `AGENTS.md` (for example, legacy smart-TV browsers freezing `<video>` on frame 0 and requiring animated WebP + ES5, or keeping a service within 5 npm packages on built-in `node:sqlite`).
2. **Spike and Stabilize ([Dan North](https://dannorth.net/blog/on-craftsmanship/)):** Build a narrow, end-to-end vertical slice from database to UI first (*Spike*) to verify the idea works in practice. Then switch to *Stabilize*: strip temporary scaffolding, handle real edge cases, and lock behavior with tests while keeping file context under 100 to 200 lines at a time.

## 2. Single Source of Truth for Shared Data

When the same domain item (projects, routes, plans, or marketing paths) is duplicated across multiple files, human and AI edits inevitably drift out of sync.

- Define shared records in a single typed module (for example `src/data/projects.ts` or `lib/constants/marketing-routes.ts`) and derive UI lists, category filters, search keywords, SEO/JSON-LD metadata, and AI context from that single export.
- Extract reusable UI components (`ProjectCard`, `ButtonLink`) when markup is genuinely shared, but follow the rule of three before introducing abstract factories or wrapper layers.

## 3. Prefer Deletion Over Addition & Small, Safe Commits

Every line of code is a maintenance and context cost. Write code that serves your team and your future self:

- **Small, frequent commits:** Commit working increments frequently so you can roll back fearlessly (especially during AI-assisted sessions) and keep Git history easy for teammates to follow. Never mix structural refactoring and behavior changes in the same commit.
- **Spot structural code smells early:** Watch for duplicated data definitions that require editing multiple files for a single change, functions that outgrow their single responsibility, and speculative abstractions.
- **Delete dead code immediately:** Remove commented-out blocks, unused imports, stale helpers, and unused props. Git preserves history.
- **Comment *why*, never *what*:** Delete comments that restate the code or echo prompt steps (`// Step 1: fetch user`). Write comments only for non-obvious constraints, browser quirks, or architectural tradeoffs.
- **No silent error swallowing:** Do not wrap typed code in defensive `try/catch` blocks that swallow errors and return `null`. Let errors surface at the boundary where recovery happens.

## 4. Document Silent Production Gotchas in `README.md`

Skip generic boilerplate in project READMEs. Beyond setup and build commands, document the **gotchas that do not throw a build error** but break silently in production:

- Cross-zone navigation (`<a href>` vs client `<Link>` across rewrites)
- Relative vs absolute API URLs under strict CORS
- `assetPrefix` and static asset paths
- Per-page canonical URLs (never hardcoding a root canonical in `layout.tsx`) and `X-Robots-Tag` indexing guards
- End-to-end smoke, asset, and canonical Playwright checks against the production build
