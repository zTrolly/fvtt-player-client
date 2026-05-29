## 2026-05-28 dependency/toolchain upgrade notes

- Upgraded to latest stable major lines while keeping Yarn 1:
  - Electron 42, Forge 7.11, Vite 8, ESLint 10, TypeScript 6, `@typescript-eslint` 8.
- Migrated lint setup from legacy `.eslintrc.json` to flat config in `eslint.config.mjs`.
- CI baseline updated from Node 18 to Node 22 and GitHub artifact actions moved to v4.
- `yarn lint` and `yarn package` are passing with upgraded stack.
- `yarn start` launches and builds targets; command was timeout-limited in this environment (app stayed running).
- Known ecosystem caveat: `eslint-plugin-import@2.32.0` reports peer range up to ESLint 9, but works for this repo with ESLint 10 in practice.
