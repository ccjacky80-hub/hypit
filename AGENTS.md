# Hypit repository guide

- This repository is the `@hypit/hypit` TypeScript/Node.js pnpm workspace. Use Node.js 22.15+ and pnpm 10.33.0.
- Install dependencies with `pnpm install`. Run the TypeScript check with `pnpm check` and the repository test suite with `pnpm test`.
- Keep changes scoped to the relevant workspace package. Do not commit credentials, local environment files, generated media, databases, or local build output.
- The repository provides the Hypit CLI, services, examples, and documentation. Treat generated production assets and deployment state as local unless a task explicitly asks to publish them.
