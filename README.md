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

## Asset and loading review checklist

This is a checklist of actions to perform, not a record of verified results.

- Inspect `app/`, `components/`, and `lib/` for local image, audio, font, or other media references. Check that each referenced file exists at the expected path and loads where used.
- Look for media files that are no longer referenced and remove only those confirmed to be unused. For media that is used, prefer files sized for their rendered role; avoid retaining unnecessarily large originals or duplicate variants.
- Review `package.json`, source imports, and the Next.js configuration for external font or script dependencies. Keep external requests only when they are intentional, and check that the page remains usable if an optional request is unavailable.
- After changing or moving assets, revisit the page and check that imports and relative paths still resolve.

## Manual review checklist

This is a checklist of actions to perform, not a record of verified results.

- Start the development server using the instructions above and open the local URL it prints. Review the app's initial page and its Möbius-style pattern.
- Try any interactions actually presented by the page or `PatternViewer`. Observe whether the pattern responds as expected; do not assume controls that are not present.
- Inspect the rendered pattern and page at a narrow mobile-sized viewport and a wide desktop-sized viewport. Check that the visualisation and any visible controls fit and remain usable.
- If you change the pattern or related logic, review the rendered result and check that imports and relative paths still resolve.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- Use Tab and Shift+Tab to check whether all controls actually presented by the page or `PatternViewer` can be reached and operated from the keyboard. Check that focus order is logical and that no interaction depends only on a pointer.
- Check that keyboard focus is clearly visible on each focused control and is not hidden by the rendered pattern or other content.
- Review visible controls for meaningful accessible names. Check whether the Möbius-style visualisation has an appropriate text description if it communicates information beyond its appearance, and whether purely decorative visual content is identified as such.
- Check text, labels, and control boundaries against their backgrounds for sufficient contrast in the rendered page; consider text placed over or near the pattern.
- If the visualisation moves or animates, check its behavior with the operating system's reduced-motion preference enabled and review whether the page remains usable with motion reduced.