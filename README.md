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

- Inventory the approved WarFighter source libraries
- Treat WarFighter **v2.10.04** as the current upstream source and v2.05 as an unpacked legacy/reference source
- Import one model, texture set, weapon, vehicle, or human asset at a time
- Recreate or adapt Gates of Hell entities and breeds as required
- Resolve material, texture, animation, skeleton, inventory, weapon, and sound dependencies
- Load and inspect assets in the Gates of Hell editor
- Perform native spawn and behavior tests where appropriate
- Record exact provenance and conversion steps
- Produce a bounded handoff package for downstream Code:4X integration

This repository should **not** contain copied Code:X assets. Code:X is a downstream runtime dependency of the Code:4X submod, not an upstream asset source for this lab.

## Source strategy

The source lineage has been corrected from direct metadata inspection:

- **Current WarFighter:** `E:\steam\steamapps\workshop\content\400750\CTA Warfighter Drop Folder`
  - nested `2777685314/mod.info` identifies **WarFighter v2.10.04**
  - current content is heavily packaged into Gates of Hell `.pak` archives
- **Legacy WarFighter reference:** `E:\warfighter_v2_05`
  - `mod.info` identifies **WarFighter v2.05**
  - useful because much of the content is already unpacked for direct inspection
- **Not WarFighter:** `E:\steam\steamapps\workshop\content\400750\2950056378`
  - its `mod.info` identifies **Rifleman Mod**
  - it is excluded from WarFighter source precedence

The current source policy is:

- **v2.10.04 is the canonical current upstream source.**
- **v2.05 is a legacy unpacked comparison/reference source.**
- Do not compare raw visible file counts between them because v2.10.04 is heavily packed.
- Do not perform a blind folder merge.
- Every imported asset records the exact source revision, archive/member path, and any approved legacy fallback.

See issue #3 for the source comparison and archive-inventory work.

## One-asset workflow

Every WarFighter addition follows the same lifecycle:

1. Select exactly one bounded asset or breed slice.
2. Identify its full dependency closure in current v2.10.04 and its v2.05 legacy counterpart where applicable.
3. Prefer the current v2.10.04 component unless a reviewed issue explicitly approves a legacy fallback.
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
- Current/legacy source choice must be explicit
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
