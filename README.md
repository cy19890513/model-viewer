# model-viewer (rebuild)

A module-by-module import of Google's [`model-viewer`](https://github.com/google/model-viewer),
rebuilt here as 10 pull requests — one package or layer per PR.

`model-viewer` is a web component for rendering interactive 3D models in the browser,
with built-in AR (WebXR / Scene Viewer / Quick Look) support. This rebuild exists for
study and experimentation with XR content experiences.

## PR map

| # | PR | Contents |
|---|----|----------|
| 1 | `chore: project scaffolding and build configuration` | Root monorepo config: package.json, lockfile, eslint, GitHub templates, build scripts (CI workflows excluded) |
| 2 | `feat: model-viewer web component core` | `model-viewer.ts`, `model-viewer-base.ts`, template, decorators, styles |
| 3 | `feat: three.js renderer layer` | `src/three-components/` — the Three.js rendering backend |
| 4 | `feat: XR features — AR mode and scene graph` | `features/ar.ts`, `features/scene-graph` — the AR/XR heart |
| 5 | `feat: remaining features` | animation, annotation, controls, environment, loading, staging |
| 6 | `feat: core utilities` | `src/utilities/` — cache eviction, progress tracking, helpers |
| 7 | `test: unit test suite` | `src/test/` specs and web-test-runner configs |
| 8 | `feat: model-viewer-effects package` | Post-processing effects package |
| 9 | `feat: space-opera sample application` | Official showcase demo app |
| 10 | `chore: docs site, fidelity tools and shared assets` | modelviewer.dev, render-fidelity-tools, shared 3D assets |

## Attribution

Original project by Google: https://github.com/google/model-viewer —
licensed under the **Apache License 2.0** (see `LICENSE`).
The `glTF-Sample-Assets` submodule is intentionally excluded from this import.
All source files are imported unmodified.
