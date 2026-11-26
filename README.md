# Noted

A responsive note-taking app implemented three ways using official Material component libraries.

## Live site

- **[Noted version selector](https://bradleysouciercomputer.github.io/Noted/)**
- [MUI version](https://bradleysouciercomputer.github.io/Noted/mui/)
- [Angular Material version](https://bradleysouciercomputer.github.io/Noted/angular/)
- [Google Material 3 version](https://bradleysouciercomputer.github.io/Noted/material3/)

## Implementations

- **MUI:** React with the official `@mui/material` and `@mui/icons-material` packages.
- **Angular Material:** a standalone Angular app using the official `@angular/material` component library.
- **Material 3:** Google's official `@material/web` web components, using the released 2.5.0 package.

## GitHub Pages deployment

The `.github/workflows/deploy.yml` workflow builds the selector and all three implementations and deploys them to GitHub Pages on each push to `main`. It can also be run manually from the Actions tab.

The source project archive is stored at `source/noted-project.tar.xz`; the workflow expands it before building.

## Local development

For the MUI and Material 3 apps:

```bash
npm install
npm run dev
```

For Angular Material:

```bash
cd apps/angular
npm install
npm start
```

## Notes and storage

Each version stores notes locally in the browser using a separate `localStorage` key. Notes do not sync between devices or between the three implementations. Clearing browser storage removes locally saved notes.

## Material Web status

The Material 3 implementation intentionally uses Google's official `@material/web` package, not a third-party recreation. The upstream project currently describes Material Web as being in maintenance mode.
