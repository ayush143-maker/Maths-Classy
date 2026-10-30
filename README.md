# Maths-Classy

An interactive mathematical-pattern visualiser built with Next.js, React, and Three.js. The page opens with a Möbius-style pattern in the shared `PatternViewer`, where visitors can explore the rendered pattern. Specific interaction controls are not described here.

## Run locally

From the project folder, install dependencies and start the development server:

    npm install
    npm run dev

Open the local URL printed by the server in your browser. Review the page after making a change. To create a production build, run:

    npm run build

## Project structure

The Next.js page is under `app/`; reusable components are under `components/`, and supporting logic is under `lib/`. `PatternViewer` is the main component to inspect when changing how patterns are rendered. At the root, `package.json` and the Next.js and TypeScript configuration files describe the project setup.