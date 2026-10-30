# Maths-Classy

A mathematical-pattern visualiser built with Next.js, React, and Three.js. It opens with a Möbius-style pattern rendered by the shared `PatternViewer` component.

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

## Project structure and customization

The Next.js page is in `app/`, reusable components are in `components/`, and supporting logic is in `lib/`. For a visible text or page-composition change, start with the relevant page in `app/`; for pattern rendering, start with `PatternViewer` in `components/` and follow any supporting logic in `lib/`.

The root includes `tailwind.config.ts` and `next.config.mjs` for project configuration. Review their existing contents before changing styling or framework settings. When moving or renaming files, update their imports and keep the existing relative paths valid. The root `package.json` and TypeScript configuration also describe project setup.