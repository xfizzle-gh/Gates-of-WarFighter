# Gates of WarFighter

**WarFighter asset import, conversion, and validation laboratory for Gates of Code:4X.**

This repository is no longer planned as a separate standalone strategic total conversion. Its purpose is to take the complete WarFighter content library approved by Yuri and port it into **Call to Arms: Gates of Hell** carefully, one asset at a time.

The downstream game project starts from **Code:X** as the gameplay/content foundation. WarFighter content is added incrementally only after it has been imported, reconstructed where needed, and proven to work correctly in the Gates of Hell editor and native game.

## Project relationship

### Gates of Code:4X

The downstream campaign/game project.

- Code:X-based submod
- Code:X remains an installed dependency rather than being copied into this repository
- Strategic overmap, factions, rosters, research, economy, AI, and campaign integration live in the Code:4X project
- WarFighter assets enter Code:4X only after passing this repository's import and validation process

The current GitHub repository for that work is `xfizzle-gh/Gates-of-Code-X`. The project may be renamed separately; this repository does not rename or redistribute Code:X.

### Gates of WarFighter

The WarFighter asset laboratory.

- Inventory approved WarFighter source material
- Maintain a complete working baseline and separately track newer current-version deltas
- Import one model, texture set, weapon, vehicle, or human asset at a time
- Recreate or adapt Gates of Hell entities and breeds as required
- Resolve material, texture, animation, skeleton, inventory, weapon, and sound dependencies
- Load and inspect assets in the Gates of Hell editor
- Perform native spawn and behavior tests where appropriate
- Record exact provenance and conversion steps
- Produce a bounded handoff package for downstream Code:4X integration

This repository should **not** contain copied Code:X assets. Code:X is a downstream runtime dependency of the Code:4X submod, not an upstream asset source for this lab.

## Source strategy

The source lineage has been corrected from direct metadata and archive inspection:

- **Complete working baseline:** `E:\warfighter_v2_05`
  - `mod.info` identifies **WarFighter v2.05**
  - 137,246 unpacked files
  - includes the broad breed, sound, humanskin, entity, vehicle, weapon, texture, and configuration trees needed for dependency-complete asset work
- **Current-version partial drop:** `E:\steam\steamapps\workshop\content\400750\CTA Warfighter Drop Folder`
  - nested `2777685314/mod.info` identifies **WarFighter v2.10.04**
  - the inspected `.pak` set contains 66,135 members and 64,893 unique normalized paths with zero archive-read failures
  - however, this local drop is **not a complete v2.10.04 distribution**: the inspected package contains no breed `.set` tree, no sound tree, only part of the humanskin library, and omits entire legacy vehicle entity families such as USA, USMC, Germany, UAF, PLA, and IDF
  - it does contain useful newer deltas, including French vehicle content, additional OPFOR entities, newer inventory/ammunition content, and thousands of current-only textures
- **Not WarFighter:** `E:\steam\steamapps\workshop\content\400750\2950056378`
  - its `mod.info` identifies **Rifleman Mod**
  - it is excluded from WarFighter source precedence

The current source policy is therefore:

- **v2.05 remains the canonical complete lab baseline until a complete v2.10.04 snapshot is acquired and verified.**
- Treat the existing v2.10.04 drop as a **newer delta/reference source**, not as a complete replacement.
- A v2.10.04 component may be selected when its dependency closure is complete and independently validated.
- Do not infer deletion from absence in the partial v2.10.04 drop.
- Do not perform a blind folder merge.
- Every imported asset records the exact source revision, archive/member path or legacy path, and any mixed-source choices.

See issue #3 for the source comparison and completeness evidence.

## One-asset workflow

Every WarFighter addition follows the same lifecycle:

1. Select exactly one bounded asset or breed slice.
2. Identify its full dependency closure in the complete v2.05 baseline and any available v2.10.04 delta.
3. Prefer a complete dependency closure over version number alone. Use v2.10.04 components where they are present and complete; otherwise retain the v2.05 component until a complete current snapshot is available.
4. Copy only that approved slice into an isolated staging area.
5. Adapt paths, materials, definitions, skeletons, inventories, and configuration for Gates of Hell.
6. Create or repair the Gates of Hell entity and breed definitions required by the asset.
7. Open the result in the Gates of Hell editor.
8. Validate model appearance, textures, materials, animations, attachment points, equipment, and behavior.
9. Spawn/test natively when editor validation alone is insufficient.
10. Record screenshots, logs, hashes, source paths, and known limitations.
11. Mark the asset `LAB ACCEPTED` only after the exact revision passes its acceptance checklist.
12. Hand the accepted package to Gates of Code:4X for a separate integration PR.

An accepted lab asset is not automatically integrated into the campaign. The downstream Code:4X repository decides faction ownership, roster placement, research placement, balance, and strategic behavior.

## Asset statuses

Each imported asset should use one of these states:

- `DISCOVERED` — present in the WarFighter inventory
- `SELECTED` — approved as the next bounded import slice
- `STAGED` — dependency closure copied into the lab workspace
- `CONVERTED` — Gates of Hell paths/configuration created
- `EDITOR PASS` — loads and renders correctly in editor
- `NATIVE PASS` — required in-game behavior/spawn checks pass
- `LAB ACCEPTED` — complete evidence and provenance recorded
- `HANDED OFF` — downstream Code:4X integration package prepared
- `INTEGRATED` — accepted by the downstream Code:4X repository

## Permission and attribution

The project owner confirms that **Yuri expressly approved use of the complete WarFighter mod and all content included with it**. This includes models, textures, materials, animations, sounds, scripts, configuration, maps, UI, branding, and supporting files.

The working permission record is maintained in [docs/ASSET_PERMISSION.md](docs/ASSET_PERMISSION.md). WarFighter-derived content remains traceable to its source and identifiable contributors. See [docs/ATTRIBUTION.md](docs/ATTRIBUTION.md).

This WarFighter approval does not grant permission to copy or redistribute Code:X. Code:X content remains external to this repository and is used only under the downstream submod relationship.

## Development rules

- One bounded asset slice per implementation PR
- No mass WarFighter dump into `main`
- No copied Code:X assets in this repository
- Complete-baseline/current-delta source choice must be explicit
- Every asset must have a dependency manifest
- Every breed/entity must be tested in editor before downstream handoff
- Native testing is required when editor inspection cannot prove behavior
- Generated or converted content must be reproducible
- Exact-head evidence before acceptance
- Independent review for foundational importer/tooling changes

See [docs/DEVELOPMENT_PRINCIPLES.md](docs/DEVELOPMENT_PRINCIPLES.md), [docs/ROADMAP.md](docs/ROADMAP.md), and [docs/ASSET_LAB_WORKFLOW.md](docs/ASSET_LAB_WORKFLOW.md).

## Credits

- **WarFighter Modification - Total Overhaul**: approved upstream asset/content library
- **Yuri**: primary WarFighter developer and permission grantor for the complete WarFighter mod and included content
- **Additional WarFighter contributors**: credited where identifiable through source records and inventory
- **Code:X**: downstream dependency/content foundation for Gates of Code:4X; Code:X content is not redistributed by this repository
- **Gates of WarFighter**: import tooling, Gates of Hell conversion work, breed/entity reconstruction, editor validation, and asset handoff

## Legal and platform notice

This is a community-created modding project. It is not affiliated with or endorsed by Digitalmindsoft, Barbedwire Studios, Valve, or the owners of third-party intellectual property represented by source material. All applicable rights remain with their respective owners.
