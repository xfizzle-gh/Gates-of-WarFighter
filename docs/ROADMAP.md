# Gates of WarFighter Roadmap

This roadmap is gate-based. Later phases may be researched in parallel, but implementation must not depend on an unaccepted earlier technical gate.

## Gate 0: Repository and approval foundation

**Goal:** Establish the rules under which the project receives, converts, credits, and publishes the fully approved WarFighter content library.

Deliverables:

- Project README and identity
- Complete WarFighter permission record
- Attribution policy
- Development and contribution rules
- Repository storage decision for large binaries
- Initial issue and pull-request conventions
- Preserved permission evidence outside public history, with an approved repository copy where appropriate

Acceptance:

- Repository documents accurately state that Yuri approved the complete WarFighter mod and all included content
- No asset category is incorrectly described as awaiting separate permission
- Provenance and contributor-credit requirements remain explicit
- The repository has an ordered execution plan

## Gate 1: WarFighter source inventory

**Goal:** Determine exactly what exists, how it is organized, what each asset depends on, and which nations and equipment families are technically complete.

Deliverables:

- Immutable source snapshot identifier
- Machine-readable file inventory with hashes
- Model, texture, material, animation, sound, script, and configuration classification
- Best-known authorship and contributor attribution per asset family
- Dependency graph for models and supporting files
- Duplicate, orphan, missing, and conflicting-file reports
- Candidate nation and equipment inventory

Acceptance:

- Inventory can be reproduced from the same source snapshot
- Every candidate model is linked to its required textures, materials, animations, and configuration
- Unknown authorship is tracked as an attribution gap, not treated as missing project permission
- Technically incomplete or missing dependencies remain visible blockers

## Gate 2: Conversion and validation pipeline

**Goal:** Build a deterministic, auditable path from approved WarFighter source files to Gates of Hell-ready output.

Deliverables:

- Import manifest schema
- Conversion toolchain and pinned environment
- Path and naming normalization
- Material and texture mapping rules
- Model validation and dependency checks
- Collision, skeleton, animation, and LOD handling policy
- Generated-output provenance and checksums
- Failure-atomic publication into a staging directory

Acceptance:

- Repeated conversion of identical inputs produces equivalent output
- Missing, malformed, or unresolved technical dependencies fail closed
- Generated files can be traced to exact source inputs and tool versions

## Gate 3: Standalone Gates of Hell shell

**Goal:** Prove that the project can load without another content mod.

Deliverables:

- Native mod metadata and folder structure
- Minimal menu and localization integration
- Clean boot with only Gates of WarFighter enabled
- One WarFighter test asset loaded through the new pipeline
- Packaging and installation checks
- Baseline log scanner

Acceptance:

- Clean installation launches with no Code:X, West81, or WarFighter dependency
- No unresolved asset paths point into another Workshop item
- Candidate build can be packaged and reinstalled reproducibly

## Gate 4: Single-faction vertical slice

**Goal:** Prove the complete tactical and strategic content path for one nation before broad expansion.

Deliverables:

- One faction identity and side mapping
- Initial infantry, specialist, vehicle, and support roster
- Research tree
- Recruitment and economy integration
- Tactical spawning and reinforcement integration
- AI availability
- Battle-result return to strategic state
- Save/load support
- Native acceptance checklist and evidence

Acceptance:

- Correct roster and research with no foreign-faction leakage
- Units can be purchased, deployed, spawned, and resolved
- Save/load preserves faction and campaign state
- Game log is clean of blocking errors

## Gate 5: Strategic overmap foundation

**Goal:** Establish the Gates of WarFighter campaign as an independent implementation of the proven overmap concept.

Deliverables:

- Strategic map data contract
- Provinces, adjacency, ownership, and movement
- Faction selection and persistence
- Economy, recruitment, research, and reinforcement contracts
- Battle generation and result import
- Fog of war and observer-safe presentation
- Deterministic save schema and migrations
- Strategic UI shell

Acceptance:

- A campaign can start, progress through multiple battles, save, reload, and continue
- Tactical results affect only authorized strategic state
- Hidden information does not leak through player or AI projections

## Gate 6: Faction expansion

**Goal:** Add nations through the accepted compiler and validation path rather than bespoke wiring.

For each faction:

- Source inventory and dependencies complete
- Canonical unit and equipment mapping
- Roster and research authored through the approved source format
- Recruitment, AI, repair, economy, reinforcement, and tactical spawn verified
- Cross-faction leakage tests
- Native-game acceptance evidence
- Attribution records updated for identifiable upstream contributors

Expansion order should be chosen after Gate 1 identifies the technically best-supported WarFighter nations. Permission is already established for the complete WarFighter content library.

## Gate 7: Campaign depth and presentation

Potential work after the core campaign is stable:

- Diplomacy and alliances
- Regional or formation-specific recruitment
- Operational conditions and modifiers
- Province development and infrastructure
- Commander or formation progression
- Expanded AI planning
- Strategic events
- Improved map presentation and accessibility
- Campaign configuration presets

Each feature requires a separate issue, bounded data contract, migration plan, and acceptance test.

## Gate 8: Release hardening

**Goal:** Produce a distributable public build with complete evidence and credits.

Deliverables:

- Full clean-install matrix
- Supported game-version declaration
- Complete asset and contributor credits
- Confirmed project-level WarFighter permission record
- Save migration and compatibility policy
- Performance and package-size review
- Workshop description and installation instructions
- Known-issues register
- Release rollback plan

Acceptance:

- No runtime dependency on another content mod
- All shipped assets are manifest-backed and traceable to the approved WarFighter source snapshot or original Gates of WarFighter work
- Native campaign smoke matrix passes
- Credits and notices are complete
- Release artifact matches the reviewed source and generated manifest
