# Gates of WarFighter Asset Lab Roadmap

This repository is an import, reconstruction, and validation laboratory for WarFighter assets that may later be integrated into Gates of Code:4X.

It is not the strategic campaign repository and is not intended to become a separate standalone total conversion.

## Gate 0: Source and provenance foundation

**Goal:** establish the approved WarFighter source authority and a reproducible way to identify every imported file.

Deliverables:

- complete WarFighter permission record
- V1/V2 source comparison
- canonical source policy
- attribution policy
- large-binary storage decision
- per-asset manifest schema

Current source policy:

- V1 (`E:\warfighter_v2_05`) is the breadth baseline
- V2 (`E:\steam\steamapps\workshop\content\400750\2950056378`) is a reconciliation/update source
- no blind V1/V2 folder merge

Acceptance:

- each source snapshot can be identified reproducibly
- asset provenance is traceable
- V1/V2 differences remain explicit

## Gate 1: Import and dependency tooling

**Goal:** build a repeatable path for selecting one WarFighter asset and collecting its complete dependency closure.

Deliverables:

- inventory/query tooling
- dependency-closure extraction
- path collision detection
- input hashing
- staging manifest
- output hashing
- conversion recipe records

Acceptance:

- a selected asset can be staged without copying unrelated faction content
- missing dependencies fail visibly
- repeated staging of the same source produces the same manifest

## Gate 2: Gates of Hell editor test harness

**Goal:** create a minimal lab environment for loading and inspecting imported WarFighter content in the Gates of Hell editor.

Deliverables:

- lab mod metadata and folder structure
- editor-visible test organization
- human/breed test area
- weapon test area
- vehicle test area
- baseline log collection
- screenshots/evidence convention

The lab must not copy Code:X assets. Code:X remains external and belongs to the downstream Code:4X project.

Acceptance:

- an imported asset can be located and loaded predictably in editor
- editor failures are attributable to the selected asset slice rather than unrelated content
- logs and evidence can be attached to the asset issue

## Gate 3: First human breed vertical slice

**Goal:** prove the full WarFighter-to-Gates-of-Hell human pipeline with exactly one infantry breed.

Required proof:

- model/body/skin load
- textures and materials resolve
- equipment attachments align
- inventory and weapon resolve
- skeleton/animations bind
- breed definition is valid
- editor spawn/inspection passes
- native movement/combat test passes if required
- `game.log` has no blocking errors from the slice

Acceptance:

- exact asset revision is marked `LAB ACCEPTED`
- dependency manifest and evidence are complete
- handoff package is ready for a separate Gates of Code:4X integration PR

## Gate 4: Repeatable one-asset intake

**Goal:** import WarFighter content incrementally rather than by faction-sized dumps.

Suggested progression:

1. additional conventional infantry breeds
2. specialists and crew breeds
3. individual weapon families
4. simple unarmed/static equipment
5. wheeled vehicles
6. tracked vehicles
7. turreted/complex vehicles
8. aircraft and highly coupled assets

Each slice receives its own issue and PR.

Acceptance for each asset:

- dependency closure complete
- Gates of Hell entity/breed/configuration valid
- editor pass
- native pass where required
- manifest and attribution complete
- exact accepted revision recorded

## Gate 5: Code:4X handoff contract

**Goal:** standardize how accepted lab assets move into the Code:X-based campaign project.

Each handoff contains:

- accepted asset files
- canonical suggested ID
- source nation/equipment identity
- provenance manifest
- runtime path requirements
- editor/native evidence
- known limitations
- collision notes against existing Gates of Hell/Code:X content

The downstream project decides roster, faction, research, cost, balance, AI use, and campaign availability.

Acceptance:

- lab acceptance and campaign integration remain separate review decisions
- Code:X files are not copied into this repository
- downstream integration can identify exactly which lab revision it consumed

## Gate 6: Library growth and maintenance

**Goal:** build a catalog of accepted WarFighter assets that can be consumed by Code:4X over time.

Maintain:

- accepted-asset registry
- superseded/replaced revision history
- V1/V2 source choices per component
- editor regression checks for previously accepted assets when tooling changes
- downstream integration references

The project should prefer steady, individually proven additions over bulk migration.
