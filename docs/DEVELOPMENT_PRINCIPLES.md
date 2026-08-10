# Development Principles

## 1. This repository is an asset lab

Gates of WarFighter exists to import, reconstruct, and validate WarFighter assets for Gates of Hell. Strategic campaign systems, nation rosters, research trees, and Code:X integration belong downstream in Gates of Code:4X.

## 2. Code:X stays external

Do not copy Code:X assets into this repository. The downstream Code:4X project is a Code:X submod and may reference Code:X under that relationship. This lab should not blur that boundary.

## 3. Full WarFighter approval is established

Yuri has approved use of the complete WarFighter mod and all included content. Inventory and provenance are technical and attribution requirements, not per-file permission gates.

## 4. One asset at a time

Default implementation scope is one human breed, one weapon family, one vehicle family, or another tightly bounded dependency-complete slice. Do not migrate a whole faction merely because the source tree makes bulk copying easy.

## 5. V1 baseline, V2 reconciliation

V1 is the canonical breadth baseline. V2 is an update/delta source. Every imported component must record its chosen source revision. Never perform an unreviewed folder overlay between the two source trees.

## 6. Dependency closure before conversion

A model is not a usable asset by itself. Resolve textures, materials, skeletons, animations, sounds, inventories, weapons, ammunition, definitions, icons, and other required files before declaring a slice staged.

## 7. Reconstruct Gates of Hell-native definitions

WarFighter content may require new or corrected Gates of Hell entities, breeds, inventories, weapon mappings, materials, attachment definitions, or configuration. These should be explicit and reviewable rather than hidden ad hoc fixes.

## 8. Editor proof is mandatory

Every breed/entity slice must be opened and inspected in the Gates of Hell editor before lab acceptance. Visual loading, materials, attachments, animations, and editor spawnability are first-class acceptance criteria.

## 9. Native proof where behavior matters

Use native Gates of Hell tests when editor inspection cannot prove movement, combat, firing, reloading, damage, vehicle interaction, sounds, effects, or other runtime behavior.

## 10. Deterministic import over manual mystery

Repeatable conversions belong in tooling or documented recipes. Record exact source paths, hashes, transformations, outputs, and tool versions. Do not accept a result that cannot be reconstructed.

## 11. Lab acceptance is not campaign acceptance

`LAB ACCEPTED` means the asset works as a Gates of Hell content slice. It does not decide faction ownership, research placement, balance, AI use, economy, or strategic availability. Those decisions belong to the downstream Code:4X integration PR.

## 12. Preserve replacement paths

A later V2 revision, corrected model, improved texture, or better breed definition may supersede an accepted asset. Stable IDs and manifests must allow replacement without losing provenance.

## 13. No unreviewed binary flood

Large binaries must be tied to an issue-authorized asset slice and manifest. Do not commit the entire WarFighter source installation or a full faction archive to `main` for convenience.

## 14. Exact-head evidence

Reports must distinguish static checks, conversion validation, editor checks, native tests, screenshots, logs, assumptions, and unresolved defects. Acceptance applies to the exact revision reviewed and tested.
