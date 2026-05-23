# IELTS Writing Lab

This is a separated version of the original standalone file:

- Source: `D:/Downloads/ielts-writing-lab-v7.html`
- App entry: `index.html`
- Styles: `styles.css`
- Editable React source: `src/*.jsx`
- Generated browser bundle: `dist/app.jsx`

## Edit Workflow

1. Edit the relevant file in `src/` or `styles.css`.
2. Rebuild the generated JSX bundle:

   ```powershell
   node scripts/build.mjs
   ```

3. Run a local static server:

   ```powershell
   node scripts/serve.mjs
   ```

4. Open `http://localhost:5173`.

The app still uses browser-side React/Babel/Chart.js from CDNs, just like the original. No npm install is required.

## Source Map

- `src/00-data.jsx`: React hook aliases and the compact AWL scheduling word list.
- `src/01-awl-card-data.jsx`: full pre-baked AWL card data, AWL lookup map, Task 1 priority set.
- `src/02-api.jsx`: AI provider presets, request wrapper, JSON cleanup parser.
- `src/03-vocab-utils.jsx`: word-card generation, morphology helpers, AWL extraction, vocab insights.
- `src/04-state.jsx`: localStorage schema, migration, schedule generation.
- `src/05-common-components.jsx`: shared UI components, word card, quiz mode, band chart.
- `src/06-dashboard.jsx`: dashboard and learning heatmap.
- `src/07-vocab.jsx`: vocabulary study, import, quiz, boost, extra sessions.
- `src/08-theory.jsx`: Task 1 guide content.
- `src/09-practice-helpers.jsx`: chart/process/map renderers, annotations, vocab insight panels.
- `src/10-practice.jsx`: question generation, essay grading, archive, revisits.
- `src/11-settings.jsx`: goals, vocab schedule, AI configuration, data management.
- `src/12-app.jsx`: navigation and root render.

## Notes

When run with `node scripts/serve.mjs`, the app syncs browser data to `data/app-state.json` in this folder. Double-clicking `index.html` still uses browser `localStorage` only. API keys are still stored in the JSON backup/localStorage, matching the original behavior, so keep this folder private.


To recopy the current Microsoft Edge localStorage into the folder JSON, run:

`powershell
node scripts/migrate-edge-localstorage.mjs
`

