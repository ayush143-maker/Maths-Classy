# Maths-Classy

An interactive mathematical-pattern visualiser built with Next.js, React, and Three.js. A shared `PatternViewer` presents explorable patterns, with a Möbius-style pattern as the starting experience.

## Run locally

Install dependencies and start the Next.js development server:

    npm install
    npm run dev

Create a production build with:

    npm run build

## Project structure

The application is organised around `app/`, reusable components, and supporting logic in `lib/`. `PatternViewer` is the main component to inspect when changing how patterns are rendered.