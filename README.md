# @exre/exui

Exre brand React component library built with Vite, Tailwind CSS v4, shadcn/ui, and Radix UI.

## Usage

Install the package in a consuming app and import the built stylesheet once:

```tsx
import "@exre/exui/style.css"
import { Button, ThemeProvider } from "@exre/exui"

export function App() {
  return (
    <ThemeProvider>
      <Button>Continue</Button>
    </ThemeProvider>
  )
}
```

## Development

```bash
pnpm install
pnpm dev
pnpm typecheck
pnpm lint
pnpm build
```

## shadcn/ui

This repository keeps shadcn/ui components as source under `src/components/ui`.

The project was initialized with:

```bash
npx shadcn@latest init --template vite --base radix --preset b5Kc86Jl4 --force -y
npx shadcn@latest add --all -y
```

Run shadcn from this package root so generated files use `components.json` and the local `@/*` alias.
