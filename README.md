# bi-pass

> TODO: Describe the product vision, target users, and primary outcomes for this project.

## Tech stack

- Next.js 14 (App Router)
- React 18 + TypeScript
- Tailwind CSS
- shadcn/ui + Radix UI primitives
- Zod for runtime validation
- Solana tooling (`@solana/web3.js`, wallet adapter packages)

## Windsprint workflow

This repo follows the windsprint workflow:

1. Bootstrap templates (`docs/guidelines.md`, `END_GOAL.md`, this `README.md`).
2. Configure CI/CD (GitHub Actions + Vercel/Kilo).
3. Implement features in small patches and group them into batches.
4. Iterate until every item in `END_GOAL.md` is checked.

- **Guidelines:** see `docs/guidelines.md`.
- **End goal:** see `END_GOAL.md`.

## Getting started

### Prerequisites

- Node 18+
- pnpm (recommended)

### Install

```bash
pnpm install
```

### Run dev server

```bash
pnpm dev
```

The app runs at [http://localhost:3000](http://localhost:3000).

### Scripts

- `pnpm dev` – start dev server
- `pnpm build` – production build
- `pnpm start` – run built app
- `pnpm lint` – run lint

## Project structure

- `app/` – Next.js app router entry
- `components/` – reusable React components
- `hooks/` – shared hooks
- `lib/` – helpers and services
- `types/` – shared TypeScript types
- `public/` – static assets

Expand this file as the project evolves (architecture, environments, deployment links, etc.).
