# Maths-Classy

Maths-Classy is an interactive mathematical-pattern visualiser built with **Next.js, React, and Three.js**. The project uses a shared PatternViewer component to present mathematical forms as visual, explorable patterns; the current starting experience is a Möbius-style pattern.

## Run locally

Install the dependencies and start the Next.js development server:

    npm install
    npm run dev

To create a production build:

    npm run build

## Project structure

The application is organised around the Next.js app/ directory, reusable components, and supporting logic in lib/. PatternViewer is the key place to look when changing how a pattern is rendered. Keep mathematical parameters, labels, and visual output consistent, and test the scene at different screen sizes.
