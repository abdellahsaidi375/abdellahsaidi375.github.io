# Graph Report - .  (2026-07-01)

## Corpus Check
- 49 files · ~92,176 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 90 nodes · 91 edges · 19 communities (13 shown, 6 thin omitted)
- Extraction: 70% EXTRACTED · 30% INFERRED · 0% AMBIGUOUS · INFERRED: 27 edges (avg confidence: 0.89)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_Project Concepts & User Rules|Project Concepts & User Rules]]
- [[_COMMUNITY_Three.js Phase 1 Pipeline|Three.js Phase 1 Pipeline]]
- [[_COMMUNITY_Phase 1 SVG Assets|Phase 1 SVG Assets]]
- [[_COMMUNITY_OpenCode Permissions|OpenCode Permissions]]
- [[_COMMUNITY_OpenCode Configuration|OpenCode Configuration]]
- [[_COMMUNITY_Sakura Flower Anatomy|Sakura Flower Anatomy]]
- [[_COMMUNITY_Camera Assets|Camera Assets]]
- [[_COMMUNITY_OpenCode Dependencies|OpenCode Dependencies]]
- [[_COMMUNITY_Glow Effects Code|Glow Effects Code]]
- [[_COMMUNITY_Glowing Icons|Glowing Icons]]
- [[_COMMUNITY_Glowing Stuff|Glowing Stuff]]
- [[_COMMUNITY_Flower Groups|Flower Groups]]
- [[_COMMUNITY_SVG Base64 Data|SVG Base64 Data]]

## God Nodes (most connected - your core abstractions)
1. `SVG-to-Three.js Rendering Pipeline` - 12 edges
2. `Interactive Instax Camera Website` - 12 edges
3. `Full Petals Composition (5 petals assembled)` - 10 edges
4. `permission` - 8 edges
5. `Full Stigma Composition (5 segments assembled)` - 8 edges
6. `Visual Parity (SVG vs Three.js)` - 5 edges
7. `Main Entry Page (Phase 1)` - 5 edges
8. `Petals.html — Phase 1 Visual Parity` - 4 edges
9. `Phase.html — Multi-SVG Combiner` - 4 edges
10. `Stamens.html — Phase 1 Visual Parity w/ Pixel Compare` - 4 edges

## Surprising Connections (you probably didn't know these)
- `Poetic Transcript` --conceptually_related_to--> `Interactive Instax Camera Website`  [INFERRED]
  graphify-out/transcripts/VID_20260501_021332.txt → context.md
- `SVG vs Three.js Visual Parity` --references--> `Main Entry Page (Phase 1)`  [INFERRED]
  compare.html → index.html
- `Glow Canvas Effect` --conceptually_related_to--> `Main Entry Page (Phase 1)`  [INFERRED]
  glow/glow/index.html → index.html
- `Retro Camera with Polaroids` --shares_data_with--> `Main Entry Page (Phase 1)`  [INFERRED]
  repo.html → index.html
- `Instax Formal Specification` --references--> `Interactive Instax Camera Website`  [EXTRACTED]
  instax.md → context.md

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Phase 1 Visual Parity Test Suite** — phase1_petals, phase1_petalsshadows, phase1_stamens, phase1_stigma, phase1_anthers [INFERRED 0.95]
- **SVG-to-Three.js Pipeline Components** — phase1_gradient_resolution, phase1_stroke_geometry, phase1_combined_geometry, phase1_gradient_texture, phase1_transform_chain [INFERRED 0.95]
- **Instax Interactive Flow** — sakura_blossom_concept, instax_camera_concept, rating_evaluation_system, language_buttons_concept [EXTRACTED 1.00]
- **OpenCode Configuration** — opencode_agents_builder_agent_doc, opencode_commands_archive_chat_command_doc, opencode_commands_organize_command_doc, opencode_skills_instax_skill_doc [EXTRACTED 1.00]
- **Three.js Graphics Suite** — black_hole_code, vortex_code, compare_svg_threejs_code, main_entry_code [INFERRED 0.85]
- **Flower Petal Assembly** — phase1_petals_petals_svg, phase1_petals_petals1_svg, phase1_petals_petals2_svg, phase1_petals_petals3_svg, phase1_petals_petals4_svg, phase1_petals_petals5_svg, phase1_petals_petals_two_svg, phase1_petals_petalsshadows_svg [EXTRACTED 1.00]
- **Flower Stigma Assembly** — phase1_stigma_stigma_svg, phase1_stigma_stigma1_svg, phase1_stigma_stigma2_svg, phase1_stigma_stigma3_svg, phase1_stigma_stigma4_svg, phase1_stigma_stigma5_svg [EXTRACTED 1.00]
- **Flower Anatomical Parts** — phase1_anthers_svg, phase1_petals_petals_svg, phase1_stamens_svg, phase1_stigma_stigma_svg [INFERRED 0.95]
- **Instax Camera Assets** — assets_img_instax_camera, assets_img_retro_camera, assets_img_retro_camera_webp [EXTRACTED 0.85]
- **Sakura Flower Components** — assets_img_sakura_svg, assets_img_sakura_petals, assets_img_sakura_stigma, assets_img_sakura_stamens, assets_img_sakura_anthers [EXTRACTED 1.00]
- **Retro Camera Image (PNG + WebP)** — assets_img_retro_camera, assets_img_retro_camera_webp [EXTRACTED 1.00]

## Communities (19 total, 6 thin omitted)

### Community 0 - "Project Concepts & User Rules"
Cohesion: 0.14
Nodes (17): Batoul (Gift Recipient), SVG vs Three.js Visual Parity, Glow Canvas Effect, Instax Camera Interface, Instax Formal Specification, Interactive Instax Camera Website, Language Buttons (AR/EN/DZ/FR), Main Entry Page (Phase 1) (+9 more)

### Community 1 - "Three.js Phase 1 Pipeline"
Cohesion: 0.21
Nodes (17): Anthers.html — Phase 1 Visual Parity w/ Pixel Compare, Combined Fill+Stroke Geometry, Curve Division / Triangulation Hypothesis, Gradient Resolution (resolveGradients), Gradient Texture Baking (makeGradientTexture), SVG Path Order Diagnostic, Petals.html — Phase 1 Visual Parity, PetalsShadows.html — Phase 1 Visual Parity (+9 more)

### Community 2 - "Phase 1 SVG Assets"
Cohesion: 0.14
Nodes (16): Anthers (flower pollen-producing parts), Individual Petal Variant 1 (lower-left petal path4740), Individual Petal Variant 2 (path4738), Individual Petal Variant 3 (path4736), Individual Petal Variant 4 (path4734), Individual Petal Variant 5 (path4721), Full Petals Composition (5 petals assembled), Simplified Two-Petal Composition (paths 4738 and 4740) (+8 more)

### Community 3 - "OpenCode Permissions"
Cohesion: 0.22
Nodes (9): *, permission, bash, edit, glob, grep, read, webfetch (+1 more)

### Community 4 - "OpenCode Configuration"
Cohesion: 0.29
Nodes (6): instructions, logLevel, $schema, shell, skills, paths

### Community 5 - "Sakura Flower Anatomy"
Cohesion: 0.40
Nodes (5): Sakura Anthers Group, Sakura Petals Group, Sakura Stamens Group, Sakura Stigma Group, Sakura Cherry Blossom SVG

### Community 6 - "Camera Assets"
Cohesion: 1.00
Nodes (3): Instax Camera, Retro Camera, Retro Camera (WebP)

## Knowledge Gaps
- **45 isolated node(s):** `@opencode-ai/plugin`, `$schema`, `logLevel`, `shell`, `websearch` (+40 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **6 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `permission` connect `OpenCode Permissions` to `OpenCode Configuration`?**
  _High betweenness centrality (0.021) - this node is a cross-community bridge._
- **Are the 7 inferred relationships involving `SVG-to-Three.js Rendering Pipeline` (e.g. with `Anthers.html — Phase 1 Visual Parity w/ Pixel Compare` and `Petals.html — Phase 1 Visual Parity`) actually correct?**
  _`SVG-to-Three.js Rendering Pipeline` has 7 INFERRED edges - model-reasoned connections that need verification._
- **Are the 3 inferred relationships involving `Full Petals Composition (5 petals assembled)` (e.g. with `Anthers (flower pollen-producing parts)` and `Full Stigma Composition (5 segments assembled)`) actually correct?**
  _`Full Petals Composition (5 petals assembled)` has 3 INFERRED edges - model-reasoned connections that need verification._
- **Are the 3 inferred relationships involving `Full Stigma Composition (5 segments assembled)` (e.g. with `Full Petals Composition (5 petals assembled)` and `Stamens (flower thread-like structures)`) actually correct?**
  _`Full Stigma Composition (5 segments assembled)` has 3 INFERRED edges - model-reasoned connections that need verification._
- **What connects `@opencode-ai/plugin`, `$schema`, `logLevel` to the rest of the system?**
  _46 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Project Concepts & User Rules` be split into smaller, more focused modules?**
  _Cohesion score 0.13970588235294118 - nodes in this community are weakly interconnected._
- **Should `Phase 1 SVG Assets` be split into smaller, more focused modules?**
  _Cohesion score 0.14166666666666666 - nodes in this community are weakly interconnected._