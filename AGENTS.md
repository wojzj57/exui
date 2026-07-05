# Repository Guidelines

## Project Structure & Module Organization

This repository is `@exre/exui`, a Vite React component library built with Tailwind CSS v4, shadcn/ui, Radix UI, and TypeScript. Source code lives in `src/`. Public package exports are collected from `src/index.ts`, shared styling is in `src/index.css`, and reusable UI primitives live under `src/components/ui`. Hooks are in `src/hooks`, helpers in `src/lib`, demo/showcase code in `src/showcase`, and static assets in `src/assets` and `public`. Build output is generated in `dist/` and should not be edited by hand.

## Documentation Locations

Use `/docs/` for maintained engineering documentation that is intended to be part of the project record. Use `/notes/` for development notes and agent-authored working material. All AI-generated reports, ADRs, RFCs, implementation plans, audits, and similar planning artifacts must be created under `/notes/`, not in `/docs/`, unless a maintainer explicitly promotes them.

## Build, Test, and Development Commands

Use pnpm 11.9.0, as declared in `package.json`.

- `pnpm install`: install dependencies.
- `pnpm dev`: start the Vite development server.
- `pnpm typecheck`: run TypeScript checks for the app config.
- `pnpm lint`: run Oxlint with React and TypeScript rules.
- `pnpm build`: typecheck, build the library, emit declarations, fix CSS typings.
- `pnpm changeset`: create a release note for user-facing package changes.
- `pnpm version-packages`: apply pending Changesets to versions and changelogs.

## Coding Style & Naming Conventions

Write TypeScript and TSX using the existing component style. Prefer named exports for public components and keep package exports explicit through `src/index.ts`. Use the configured `@/*` aliases from `components.json`, for example `@/components/ui/button` and `@/lib/utils`. Keep shadcn/ui source components under `src/components/ui` and avoid unrelated rewrites of generated component structure. Oxlint enforces hook correctness and warns when files mix component exports with non-component exports.

## Testing Guidelines

Follow the engineering testing policy in `TESTING.md`. If that file is not present yet, keep changes conservative and run at least `pnpm typecheck`, `pnpm lint`, and `pnpm build`. There is currently no dedicated `pnpm test` script. When adding test infrastructure, document naming conventions, placement, and commands in `TESTING.md`.

## Commit & Pull Request Guidelines

Follow contribution and commit requirements in `CONTRIBUTING.md`. The current convention is Conventional Commits: `feat:`, `fix:`, `docs:`, `test:`, `refactor:`, and `chore:`. Include a DCO sign-off in commits. Pull requests should summarize the user-facing change, list validation commands run, link related issues, and include screenshots or recordings for visual component changes. Add a Changeset for release-worthy package behavior or API changes.
