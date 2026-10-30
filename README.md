# Maths-Classy

Maths-Classy is a mathematical-pattern visualiser built with Next.js, React, and Three.js. It opens with a Möbius-style pattern rendered by the shared `PatternViewer` component.

## Run locally

From the project folder, install dependencies and start the development server:

```sh
npm install
npm run dev
```

Open the local URL printed by the server. To create a production build, run:

```sh
npm run build
```

## Project structure

- `app/` — Next.js pages and page composition.
- `components/` — reusable interface components, including `PatternViewer`.
- `lib/` — supporting logic used by the application.
- `package.json` — dependencies and declared scripts.
- `next.config.mjs` and `tailwind.config.ts` — Next.js and Tailwind configuration.

For visible text or page composition, start with the relevant file in `app/`. For pattern rendering, inspect `PatternViewer` in `components/` and follow its supporting logic into `lib/`. When moving or renaming files, update affected imports and keep relative paths valid.

## Configuration and changes

Review the existing configuration files before changing framework or styling settings. The root TypeScript configuration and `package.json` also describe the project setup. Keep pattern changes scoped to the relevant page, component, or supporting logic, and review the rendered result after changes.

The documented commands support local development and a production build; no hosting provider or deployment configuration is specified. The build command alone does not determine how a separate publishing workflow should serve the application.