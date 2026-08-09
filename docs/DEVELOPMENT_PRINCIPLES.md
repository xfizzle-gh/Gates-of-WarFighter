# Development Principles

## 1. Standalone means standalone

A released Gates of WarFighter build must install and run without Code:X, West81, WarFighter, Gates of Code:X, or another content mod. Development tools may inspect approved WarFighter source material, but runtime files must not resolve assets through another Workshop installation.

Standalone acceptance requires testing against a clean Gates of Hell installation with only the candidate build enabled.

## 2. Full WarFighter approval is established

Yuri has approved use of the complete WarFighter mod and all content included with it for Gates of WarFighter. Models, textures, materials, animations, audio, scripts, configuration, maps, UI, branding, and supporting files do not require separate asset-category permission decisions.

Inventory and provenance remain mandatory so every imported asset can be traced, reproduced, credited, and validated technically.

## 3. Port the complete content library, rebuild the product

The project may reuse the approved WarFighter content library, including source configuration where technically useful, but Gates of WarFighter should be deliberately rebuilt as a standalone Gates of Hell product.

Factions, rosters, research, campaign behavior, AI integration, packaging, and strategic systems should be adapted or recreated for the new technical foundation rather than preserving hidden runtime dependencies on the original Workshop item.

## 4. Deterministic import over manual mutation

Repeatable conversions belong in tools. Generated output must identify its source inputs, tool version, configuration, and hashes. Generated files must not be hand-edited in ways that cannot be reproduced.

Raw approved sources, conversion workspaces, generated intermediates, and release output should remain clearly separated.

## 5. Small, ordered pull requests

Each pull request should deliver one bounded gate or vertical slice. Foundational contracts merge before content depends on them.

Pull requests remain draft until their implementation, focused tests, documentation, and acceptance evidence are complete. Review and testing apply to the exact head proposed for merge.

## 6. One source of truth

Faction identities, unit identifiers, research relationships, asset mappings, and generated output should each have a canonical authority. Parallel handwritten copies invite drift and should be avoided.

## 7. Validate semantics, not only file presence

A successful conversion is not proven by files existing. Validation should confirm that models load, materials resolve, animations bind, units spawn, faction ownership is correct, research unlocks the intended content, save/load works, and logs remain clean.

## 8. Protect the strategic layer from content assumptions

The overmap should consume explicit faction and capability contracts rather than hardcoded knowledge of the source Workshop installation. This allows factions and assets to evolve without silently corrupting campaign state.

## 9. Preserve a replacement path

Imported assets may later require correction, optimization, or replacement. Stable identifiers and manifests should allow an asset to be replaced without rewriting unrelated strategic or roster data.

## 10. Evidence before expansion

The project should prove one complete faction vertical slice before multiplying the content surface. The vertical slice must include standalone boot, roster, research, recruitment, tactical spawn, battle result return, save/load, and clean logs.

## 11. No unreviewed binary flood

Large assets require an approved storage and review strategy. Binary additions should be grouped by documented inventory slices, not committed as an unauditable archive dump.

## 12. Honest status reporting

Reports must distinguish completed work, generated output, tests actually executed, manual checks, assumptions, attribution gaps, and technical risks. A green script cannot substitute for native-game acceptance.
