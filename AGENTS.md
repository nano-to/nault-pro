# AGENTS.md

- Repo is an Angular 13 app with an Electron desktop shell.
- Web bootstrap starts at `src/main.ts`; app wiring is in `src/app/app.module.ts`.
- Electron bootstrap is `desktop-app/src/desktop-app.ts`.
- Use `npm` here; the repo is locked with `package-lock.json`.
- GitHub compare against `nault/nault` master currently shows this fork 180 commits ahead.

## Commands

- `npm install` installs dependencies.
- `npm run start` or `npm run wallet:dev` starts the Angular dev server.
- `npm run build` builds the web app into `docs/`.
- `npm run wallet:build` is the production web build.
- `npm run wallet:build-desktop` builds the desktop web bundle with `environment.desktop.ts`.
- `npm run lint` runs Angular ESLint.
- `npm run test` runs Karma tests in Chrome and stays in watch mode.
- `npm run e2e` runs Protractor against `http://localhost:4200/`; start the dev server first.
- `npm run desktop:compile` compiles Electron TS into `desktop-app/dist/`.
- `npm run desktop:build` builds the desktop web bundle, then compiles Electron.
- `npm run desktop:dev` runs the desktop app from the compiled Electron entrypoint.
- `npm run desktop:local` packages the desktop app locally.
- `npm run release` is the full desktop packaging path.

## Repo Quirks

- Treat `docs/`, `desktop-app/dist/`, and `desktop-app/build/` as generated output.
- Desktop builds use `src/environments/environment.desktop.ts`; production web builds use `src/environments/environment.prod.ts`.
- Service worker registration is enabled only for production web builds, not desktop builds.
- CI linting on Linux installs `build-essential`, `git`, `libudev-dev`, and `libusb-1.0-0-dev` before `npm run lint`.
