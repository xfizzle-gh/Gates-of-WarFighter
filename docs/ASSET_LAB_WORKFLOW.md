# WarFighter Asset Lab Workflow

## Purpose

This repository exists to turn individual WarFighter assets into tested Gates of Hell-ready content that can be handed to Gates of Code:4X.

The unit of work is intentionally small. A pull request should normally contain one human breed, one weapon family, one vehicle family, or another tightly bounded dependency-complete slice.

## Source authority

Two approved WarFighter source trees are currently available:

- V1: `E:\warfighter_v2_05`
- V2: `E:\steam\steamapps\workshop\content\400750\2950056378`

V1 is the canonical breadth baseline. V2 is a reconciliation source for later or divergent files. Never copy V2 over V1 globally.

For every asset, the manifest must record the chosen source for each component, including model, textures, materials, animation/skeleton data, definition files, sounds, icons, inventories, weapons, and supporting configuration.

## Asset slice lifecycle

### 1. Select

Create or assign an issue for exactly one bounded asset slice.

Record:

- canonical working name
- source faction/nation
- V1 paths
- V2 paths if present
- intended downstream use
- known dependencies
- expected Gates of Hell entity/breed type

### 2. Resolve dependency closure

Before conversion, identify every file the asset requires.

For a human/breed this normally includes:

- human model/body components
- humanskin definitions
- textures/materials
- skeleton/animation assumptions
- headgear and equipment attachments
- inventory definition
- weapon and ammunition definitions
- breed definition
- localization/display name where required

For vehicles this normally includes:

- model and LODs
- collision/physics data
- textures/materials
- turret/weapon definitions
- crew positions
- sounds/effects
- damage configuration
- vehicle entity definition

Missing dependencies must be reported before editor testing.

### 3. Stage

Copy only the dependency-complete slice into the lab staging tree. Do not copy an entire source faction or Workshop directory for convenience.

Record input hashes before modification.

### 4. Convert and reconstruct

Adapt the selected content for Gates of Hell.

Typical work includes:

- path normalization
- material and texture reference correction
- entity inheritance correction
- breed recreation
- inventory/loadout reconstruction
- weapon/ammunition mapping
- skeleton and attachment validation
- animation mapping
- collision and LOD correction
- localization and editor naming

Do not depend on Code:X files inside the lab. The asset must be understandable and testable as a WarFighter-to-Gates-of-Hell conversion slice.

### 5. Editor validation

Open the exact staged asset in the Gates of Hell editor and capture evidence.

Human/breed acceptance should check at least:

- entity loads without missing-resource errors
- body/skin renders correctly
- textures and materials resolve
- head, hands, gear, and attachments align
- weapon is held correctly
- idle/movement/combat animations bind correctly
- no obvious mesh explosions, T-pose, invisible components, or wrong-material surfaces
- breed is selectable/spawnable through the intended editor path

Vehicle acceptance should check at least:

- model and LODs render correctly
- textures/materials resolve
- turrets, weapons, hatches, wheels/tracks, and crew positions align
- collision/physics representation is plausible
- weapon mounts and effects originate from correct locations
- no missing components or obvious visual corruption

### 6. Native validation

Run native Gates of Hell checks when editor inspection cannot prove behavior.

Examples:

- spawn the breed in a test mission
- move and animate the soldier
- fire/reload/switch weapons
- enter/exit vehicles
- fire vehicle weapons
- receive damage and die
- confirm sounds/effects
- inspect `game.log`

### 7. Lab acceptance

An asset becomes `LAB ACCEPTED` only when:

- all required source files are manifest-backed
- conversion steps are reproducible
- editor evidence is attached
- native tests required by the slice pass
- no blocking missing-resource or parse errors remain
- known visual/behavioral limitations are documented
- exact accepted revision/hash is recorded

### 8. Downstream handoff

Prepare a compact handoff for Gates of Code:4X containing:

- accepted asset files
- manifest and source provenance
- required runtime paths
- screenshots/evidence
- known limitations
- suggested canonical ID
- source nation/equipment identity
- integration notes

The downstream Code:4X PR decides:

- faction ownership
- roster placement
- research placement
- balance and cost
- campaign availability
- AI use
- strategic behavior

The asset lab does not make those campaign decisions.

## Naming and collision policy

Do not overwrite an existing Code:X or Gates of Hell asset merely because a WarFighter asset has the same real-world name. Use a stable lab identity until downstream integration chooses whether the WarFighter version replaces, supplements, or coexists with an existing asset.

## Evidence standard

Every accepted asset should retain:

- exact source paths
- input hashes
- output hashes
- conversion recipe/tool version
- changed-file list
- editor screenshots
- native test notes when applicable
- relevant log excerpts
- exact accepted Git commit

## Preferred first slices

Start with simple human breeds before complex vehicles. A single infantryman with a conventional weapon tests the most important human-model, skin, material, attachment, inventory, weapon, and animation seams with a manageable dependency surface.

After the human pipeline is proven, add progressively more complex specialists, weapons, and vehicles one at a time.
