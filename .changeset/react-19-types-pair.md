---
"@localyze-pluto/components": minor
"@localyze-pluto/theme": minor
---

Move @types/react and @types/react-dom to 19.x together

@types/react-dom@19 declares `peerDependencies: { "@types/react": "^19.3.0" }`, so the
two must be bumped as a pair. Also pins both in root `resolutions` to collapse the
duplicate React type trees that `@types/styled-components` pulled in transitively, and
adds an explicit `@types/prop-types` (previously supplied by `@types/react@18`).
