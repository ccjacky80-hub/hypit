# Hypit repository guide

- This repository is the `@hypit/hypit` TypeScript/Node.js pnpm workspace. Use Node.js 22.15+ and pnpm 10.33.0.
- Install dependencies with `pnpm install`. Run the TypeScript check with `pnpm check` and the repository test suite with `pnpm test`.
- Keep changes scoped to the relevant workspace package. Do not commit credentials, local environment files, generated media, databases, or local build output.
- The repository provides the Hypit CLI, services, examples, and documentation. Treat generated production assets and deployment state as local unless a task explicitly asks to publish them.

## Video production workflow

- Follow `docs/VIDEO_WORKFLOW.md` for production handoffs and project structure.
- ChatGPT owns reference analysis, creative direction, script, shot list, final prompts, the first Hypit/SVML draft, and video quality review.
- Codex owns environment and dependency checks, CLI execution, authorized Jimeng CLI generation, Hypit build/debug/render, and reporting results.
- Do not reinterpret or redesign decisions marked `LOCKED` in project documents. If execution is blocked by a locked decision, report the conflict and ask for direction.
- Save final Google Flow prompts to `projects/<project-id>/prompts/flow/shot_XXX.txt` and final Jimeng prompts to `projects/<project-id>/prompts/jimeng/shot_XXX.txt`. Chat messages are not the only record.
- Keep generated video clips under `projects/<project-id>/assets/video/` and final renders under `projects/<project-id>/output/`.
- Project-specific execution rules in `projects/AGENTS.md` apply to all project folders, including `_template` copies.
