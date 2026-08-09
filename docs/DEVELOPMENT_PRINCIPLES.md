# Development Principles

## 1. Standalone means standalone

A released Gates of WarFighter build must install and run without Code:X, West81, WarFighter, Gates of Code:X, or another content mod. Development tools may inspect authorized source material, but runtime files must not resolve assets through another Workshop installation.

Standalone acceptance requires testing against a clean Gates of Hell installation with only the candidate build enabled.

## 2. Permission and provenance are entry gates

Asset import begins with an inventory and permission decision, not a bulk copy. Unknown authorship, unclear dependencies, or missing evidence block public integration.

Every imported asset must be traceable from an upstream source to a destination file through a machine-readable manifest.

## 3. Port assets, rebuild the product

The project may reuse authorized visual source material, but it should not casually transplant WarFighter's entire implementation. Gates of Hell configuration, factions, rosters, research, campaign behavior, AI integration, and packaging should be deliberately rebuilt for this project.

Source code or configuration from WarFighter may be studied or reused only when its permission and technical suitability are separately established.

## 4. Deterministic import over manual mutation

Repeatable conversions belong in tools. Generated output must identify its source inputs, tool version, configuration, and hashes. Generated files must not be hand-edited in ways that cannot be reproduced.

Raw authorized sources, conversion workspaces, generated intermediates, and release output should remain clearly separated.

## 5. Small, ordered pull requests

Each pull request should deliver one bounded gate or vertical slice. Foundational contracts merge before content depends on them.

Pull requests remain draft until their implementation, focused tests, documentation, and acceptance evidence are complete. Review and testing apply to the exact head proposed for merge.

## 6. One source of truth

Faction identities, unit identifiers, research relationships, asset mappings, and generated output should each have a canonical authority. Parallel handwritten copies invite drift and should be avoided.

## 7. Validate semantics, not only file presence

A successful conversion is not proven by files existing. Validation should confirm that models load, materials resolve, animations bind, units spawn, faction ownership is correct, research unlocks the intended content, save/load works, and logs remain clean.

## 8. Protect the strategic layer from content assumptions

The overmap should consume explicit faction and capability contracts rather than hardcoded knowledge of a particular source mod. This allows factions and assets to evolve without silently corrupting campaign state.

## 9. Preserve a replacement path

Imported assets may later require correction or removal. Stable identifiers and manifests should allow an asset to be replaced without rewriting unrelated strategic or roster data.

## 10. Evidence before expansion

The project should prove one complete faction vertical slice before multiplying the content surface. The vertical slice must include standalone boot, roster, research, recruitment, tactical spawn, battle result return, save/load, and clean logs.

## 11. No unreviewed binary flood

Large assets require an approved storage and review strategy. Binary additions should be grouped by documented inventory slices, not committed as an unauditable archive dump.

## 12. Honest status reporting

Reports must distinguish completed work, generated output, tests actually executed, manual checks, assumptions, and unresolved rights or technical risks. A green script cannot substitute for native-game acceptance.
