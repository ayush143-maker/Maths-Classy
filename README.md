# Maths-Classy

Maths-Classy is a mathematical-pattern visualiser built with Next.js, React, and Three.js. It opens with a Möbius-style pattern rendered by the shared `PatternViewer` component. The configured pattern list contains seven IDs: Möbius, Hopf Fibration, Butterfly, Rose, Lorenz, Fibonacci, and Torus.

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

## Project structure and rendering

- `app/` — Next.js pages and page composition.
- `components/` — reusable interface components, including `PatternViewer`.
- `lib/` — supporting logic used by the application.
- `package.json` — dependencies and declared scripts.
- `next.config.mjs` and `tailwind.config.ts` — Next.js and Tailwind configuration.

For visible text or page composition, start with the relevant file in `app/`. For pattern rendering, inspect `PatternViewer` in `components/` and follow its supporting logic into `lib/`. When moving or renaming files, update affected imports and keep relative paths valid.

`PatternViewer` procedurally builds point positions and hues for the supplied pattern and renders them as a full-screen Three.js WebGL point cloud. The visualization rotates, subtly scales, changes color, and cycles through build, hold, and dissolve phases. Its animation advances by a fixed `0.016` per frame. The component responds to window resizing and cleans up its animation frame, resize listener, geometry, material, and renderer when the effect is cleaned up or the pattern changes.

The viewer accepts a pattern prop, but the supplied component contains no pattern-selection controls. The configured pattern IDs therefore describe available rendering configurations, not a demonstrated in-viewer selector. The supplied files show no persistence or external provider calls.

## Configuration and changes

Review the existing configuration files before changing framework or styling settings. The root TypeScript configuration and `package.json` also describe the project setup. Keep pattern changes scoped to the relevant page, component, or supporting logic, and review the rendered result after changes.

The documented commands support local development and a production build; no hosting provider or deployment configuration is specified. The build command alone does not determine how a separate publishing workflow should serve the application.