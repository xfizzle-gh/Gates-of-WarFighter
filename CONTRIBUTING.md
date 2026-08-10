# Contributing to Gates of WarFighter

## Purpose

This repository is a WarFighter-to-Gates-of-Hell asset lab. Contributions should make one bounded WarFighter asset slice work correctly in Gates of Hell and produce evidence suitable for downstream Gates of Code:4X integration.

Read:

- `README.md`
- `docs/ASSET_PERMISSION.md`
- `docs/ATTRIBUTION.md`
- `docs/DEVELOPMENT_PRINCIPLES.md`
- `docs/ROADMAP.md`
- `docs/ASSET_LAB_WORKFLOW.md`

## Source boundaries

Yuri approved use of the complete WarFighter mod and all included content.

Code:X is different: do not copy Code:X assets, source files, or binaries into this repository. Code:X remains an external dependency of the downstream Code:4X submod.

## Issue-first workflow

Every asset-import PR must have an issue defining:

- exact asset/breed/weapon/vehicle slice
- V1 and V2 source paths
- selected canonical source per component
- expected dependency closure
- Gates of Hell entity/breed/configuration work
- editor acceptance checks
- native checks when required
- expected files and binaries
- provenance/attribution updates
- explicit exclusions

Do not broaden the PR into neighboring assets or a whole faction.

## Pull requests

Open implementation PRs as drafts until evidence is complete.

A PR must report:

1. issue served
2. exact asset slice
3. V1/V2 source decision
4. complete changed-file list
5. dependency manifest
6. conversion/reconstruction work
7. tests actually executed
8. Gates of Hell editor checks actually performed
9. native tests actually performed
10. screenshots/log evidence
11. known limitations
12. exact head commit submitted for acceptance

## Asset manifest

Every imported or converted asset must record at least:

- stable lab asset ID
- upstream WarFighter source tree and relative paths
- V1/V2 source choice per component
- input hashes
- dependency list
- original author or best-known contributor where identifiable
- permission basis: complete WarFighter approval from Yuri
- conversion recipe/tool version
- destination paths
- output hashes
- editor status
- native-test status
- accepted Git revision
- downstream Code:4X handoff/integration reference when applicable

## Editor evidence

A human/breed PR should normally prove:

- model/body/skin load correctly
- textures/materials resolve
- equipment and attachments align
- weapon/inventory resolve
- skeleton and animations bind
- breed is selectable/spawnable through the intended editor flow
- no obvious T-pose, invisible geometry, exploded mesh, missing material, or misplaced equipment

Vehicle and weapon slices require equivalent asset-specific checks.

## Native testing

Run native Gates of Hell tests whenever editor inspection cannot prove runtime behavior. Do not claim a native pass based only on editor loading.

Inspect `game.log` for blocking parse, missing-resource, inheritance, animation, material, sound, or spawn errors attributable to the slice.

## Generated content

Generated files must be reproducible from committed tooling/configuration or a precise documented recipe. Do not hand-edit generated output without updating its source authority.

## Commit hygiene

- one bounded asset slice per PR
- no unrelated cleanup
- no full Workshop source dumps
- no copied Code:X content
- no force-push of an accepted head without fresh review
- no merge around unresolved blocking editor/native findings

## Lab acceptance and downstream integration

A `LAB ACCEPTED` asset is ready for handoff, not automatically part of Gates of Code:4X.

The downstream repository separately decides faction ownership, roster/research placement, costs, balance, AI usage, and campaign integration.
