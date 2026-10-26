# figma-make-web-test

A deliberately small **Vue 3 + Vite + TypeScript** project used to evaluate whether
AI coding agents (specifically **Figma Make**) can clone a real repository, install
dependencies, run the dev server, modify code, and push changes back to GitHub.

This is a test fixture, **not** a production application.

## Tech stack

| Layer | Choice |
| --- | --- |
| Framework | Vue 3 (`<script setup>` SFCs) |
| Build tool | Vite |
| Language | TypeScript |
| Styling | Plain CSS |
| Runtime / package manager | Node.js + npm |

## Requirements

- Node.js 20.19+ (tested with Node.js v24.19.0)
- npm 10+ (tested with npm 11.17.0)

## Getting started

```bash
npm install
npm run dev
```

The dev server prints a local URL, usually <http://localhost:5173/>.

## Build and preview

```bash
npm run build
npm run preview
```

`npm run build` type-checks the project with `vue-tsc` and writes the production
bundle to `dist/`. `npm run preview` serves that bundle locally.

## What is on the page

- Heading: **Figma Make Web Test**
- A counter button that increments on every click
- A visible baseline marker: `FIGMA_WEB_BASELINE_20261026`

## Project structure

```text
.
├── index.html          # Vite HTML entry
├── package.json        # scripts: dev / build / preview
├── public/
│   └── favicon.svg
├── src/
│   ├── App.vue         # page, counter, baseline marker
│   ├── main.ts         # app bootstrap
│   └── style.css       # global styles
├── tsconfig.json       # TypeScript project references
├── tsconfig.app.json
├── tsconfig.node.json
└── vite.config.ts
```

## Baseline marker

`FIGMA_WEB_BASELINE_20261026` is defined in `src/App.vue` and rendered on the page.
Keep it intact when making experimental changes so the original baseline can be
identified.

## Suggested Figma Make exercises

1. Clone this repository and run `npm install` + `npm run dev`.
2. Change the heading or button label and observe hot reload.
3. Add a small component (for example, a list) and keep the counter working.
4. Create a branch, commit the change, and push it back to GitHub.
