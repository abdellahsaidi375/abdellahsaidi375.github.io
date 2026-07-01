# Instax Project — Agent Guide

## Project structure
- Root `index.html` — main interactive experience (sakura fall → camera → rating).
- `repo.html` — standalone retro camera + polaroid desk (ported from HeftyKoo/retro-camera).
- `.PHASE1/` — SVG→Three.js visual parity test suite (SVG source files + compare HTML files).
- `glow/` — experimental glow/canvas effects (not integrated).
- `graphify-out/` — knowledge graph artifacts (90 nodes, 91 edges). Use `graphify query "<q>"` to explore.
- `context.md` — full user spec (final authority). `instax.md` — structured phase-by-phase breakdown.

## No build system
Vanilla HTML/CSS/JS only. No npm scripts, bundler, server, or CI. Serve locally with `http-server`, `npx serve`, or open via any static file server (not `file://` — CDN imports and fetch will fail).

## Three.js dependency
Pinned to Three.js `0.162.0` via CDN importmap in every HTML file. Do not bump version without testing visual parity. Import map pattern:
```html
<script type="importmap">
  { "imports": {
      "three": "https://unpkg.com/three@0.162.0/build/three.module.js",
      "three/addons/": "https://unpkg.com/three@0.162.0/examples/jsm/"
  }}
</script>
```

## Two rendering approaches in parallel
- **index.html** — `buildHierarchy()` manually parses SVG XML + `SVGLoader` paths, resolves gradients, builds Three.js groups by `<g>` id. Uses `resolveGradients` → `makeGradientTexture` pipeline.
- **Phase1/compare.html** — pure `SVGLoader.toShapes()` with custom `makeStrokeGeometry()` + `makeGradientTexture()` per-pixel shader. Different transform handling.

Both produce slightly different output — visual parity is an active investigation.

## Code conventions (enforced)
- Every function must have `//#explaining_the_function#` comment above it.
- Full block replacement when modifying (no patching). Call entire function/CSS rule, rewrite cleanly, replace.
- ID-based scope isolation: each stage/effect bound to a specific HTML `id`.
- No external frameworks or libraries beyond Three.js importmap. Vanilla JS only.
- `archive_chat` command: `echo 'Generating smart compound log...'` then structured summary.
- `organize` command: adds `//#explaining_the_function#` above each function.

## Key files by phase
| Phase | File(s) |
|---|---|
| 1 (Sakura fall) | `index.html` (lines ~73–96 physics, ~476–530 animation loop) |
| 2 (Camera) | `repo.html` (retro camera + polaroid system), context.md Phase 2 spec |
| 3 (Voice/sun) | context.md Phase 3 — audio onended chaining |
| 4 (Signature + glass) | context.md Phase 4 — marquee ribbons + engraved name + glass slider |
| 5 (Final/buttons) | context.md Phase 5 — rating GIF reactions + language buttons |

## SVG anatomy (sakura.svg)
Four named `<g>` groups: `Petals`, `Stigma`, `Stamens`, `Anthers`. The SVG has `userSpaceOnUse` gradients with `gradientTransform` matrix attributes. Gradient resolution in `resolveGradients()` handles both `linearGradient`/`radialGradient` and `xlink:href` inheritance.

## Testing
No test framework. Visual parity is verified manually via `compare.html` (pixel diff between native SVG canvas render and Three.js render). Active investigation: `triangulation_test.html` in `.PHASE1/`.

## Shell
PowerShell 7+ (`pwsh`). Use `&&` for pipeline chaining.

## OpenCode agents
- `builder` subagent (`.opencode/agents/builder.md`) — must consult user before writing full implementations.
- `instax` skill (`.opencode/skills/instax/SKILL.md`) — covers flow steps and style rules.

## Gotchas
- SVG paths use `userSpaceOnUse` gradients with `gradientTransform`. The `makeGradientTexture()` bbox mapping is critical to visual parity — small errors produce visible pixel diffs.
- `SVGLoader.toShapes()` bakes element transforms into geometry. Do not double-apply transforms (common bug in `applySVGTransform` calls).
- `index.html` loads SVG from `src/img/sakura.svg` (relative path) — must run from server root, not subdirectory.
- Fonts `ArefRuqaa-Bold.ttf` and `DaveMoris.otf` in `assets/fonts/` — needed for Phase 4 marquee/signature.
- `graphify-out/` is a knowledge graph, not source code. Use `graphify query` for focused questions.
