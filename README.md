# Maths-Classy

An interactive mathematical-pattern visualiser built with Next.js, React, and Three.js. A shared `PatternViewer` presents explorable patterns, with a Möbius-style pattern as the starting experience.

## Run locally

From the project folder, install dependencies and start the development server:

    npm install
    npm run dev

Open the local URL printed by the server in your browser.

To create a production build, run:

    npm run build

## Project structure

The application is organised around `app/`, reusable components, and supporting logic in `lib/`. `PatternViewer` is the main component to inspect when changing how patterns are rendered.