# Project Guidelines

This document is the source of truth for how we build and evolve **bi-pass**.

## Languages & frameworks

- TypeScript only (no plain `.js` in source where we control it).
- React + Tailwind CSS for all UI.
- Next.js 14 App Router for the web app.

## Architecture & structure

- `app/` as the main web entry.
- Prefer small, focused, composable components (atomic design).
- Shared types live in `types/` and are reused across the codebase.
- Use Zod (or compatible) for runtime validation at API and boundary layers.

If we later adopt an Nx monorepo, we will standardize around:

- `apps/` – platform-specific apps (web, mobile, desktop).
- `libs/` – shared types, UI, and business logic.

## Windsprint workflow

The dev flow follows the windsprint **patch → batch → release** spiral:

1. Implement a small, well-defined patch (feature or fix).
2. Group patches into a batch (milestone).
3. Deploy via CI/CD (GitHub Actions + Vercel/Kilo).
4. Run user tests and compare against `END_GOAL.md`.

Each patch should:

- Reference at least one checkbox item in `END_GOAL.md`.
- Update documentation (for example under `docs/patches/`) once that structure exists.

## Testing & quality

- Add/maintain Jest tests for units and integration points as we introduce testing.
- Aim for ≥90% coverage on critical paths before closing a batch.
- Use TypeScripts strict mode and fix type errors before merging.

## Git & tagging

- Prefer small, focused commits.
- Use semantic commit messages when practical.
- Tags follow semantic versions: `v0.0.1`, `v0.1.0`, etc.
- `v0.0.1` corresponds to the initial bootstrap of templates + project setup.

## Evolving this document

Keep this file updated as conventions change. Treat it as a living spec rather than a snapshot.
