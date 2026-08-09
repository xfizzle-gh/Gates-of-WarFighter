# Gates of WarFighter

**Modern war, fought one province at a time.**

Gates of WarFighter is a standalone modern-warfare total conversion for **Call to Arms: Gates of Hell**. It combines a persistent strategic overmap campaign with real-time tactical battles using the complete WarFighter content library with express approval from Yuri.

## Project identity

Gates of WarFighter is being built as an independent Gates of Hell mod:

- No Code:X dependency
- No West81 dependency
- No WarFighter Workshop dependency at runtime
- No other content-mod dependency planned for the core experience
- The complete WarFighter content library is approved for use in this project
- Factions, rosters, research, campaign progression, AI integration, and strategic systems are rebuilt specifically for Gates of Hell

The strategic campaign is based on the overmap concept developed for Gates of Code:X, but this repository has its own technical foundation, content pipeline, release packaging, and acceptance process.

## Intended experience

Players will choose a modern nation, develop its military, research new capabilities, recruit authentic formations, expand across a persistent operational map, and personally command the battles that determine control of each region.

Planned pillars include:

1. Standalone installation and launch
2. Authorized WarFighter models, textures, materials, animations, sounds, configurations, and supporting content ported to Gates of Hell
3. Nation-specific rosters and research trees
4. Persistent strategic conquest over an operational map
5. Tactical battles driven by strategic state
6. Save/load integrity and deterministic content generation
7. Auditable asset provenance and complete contributor attribution

## Current status

**Pre-production / repository foundation.**

The first development gates are source inventory, deterministic conversion, clean standalone boot, and one vertical-slice faction. Broad content import must follow the approved technical and provenance pipelines, but it does not require separate permission for individual WarFighter asset categories.

See [the roadmap](docs/ROADMAP.md) and the repository issues for the ordered implementation plan.

## Asset permission and attribution

The project owner confirms that **Yuri expressly approved use of the complete WarFighter mod and all content included with it for Gates of WarFighter**. This approval includes the models, textures, materials, animations, sounds, scripts, configuration, maps, UI, branding, and supporting files needed to port and rebuild the experience as a standalone Gates of Hell mod.

The working permission record is maintained in [docs/ASSET_PERMISSION.md](docs/ASSET_PERMISSION.md). WarFighter-derived content must remain identifiable in the project inventory and credits. See [docs/ATTRIBUTION.md](docs/ATTRIBUTION.md).

Approval to use the complete WarFighter content library does not transfer ownership or remove the obligation to credit Yuri and other identifiable contributors.

## Development rules

The project follows a gate-based, reviewable workflow:

- One bounded implementation slice per pull request
- Draft pull requests until acceptance evidence is complete
- Exact-head review and testing
- Generated content must have a reproducible source and process
- Imported assets must have recorded provenance
- No hidden dependency on another Workshop mod
- No broad asset dump directly into `main`
- Independent review before foundational gates merge

See [docs/DEVELOPMENT_PRINCIPLES.md](docs/DEVELOPMENT_PRINCIPLES.md) and [CONTRIBUTING.md](CONTRIBUTING.md).

## Repository layout

The final source layout will be established by the foundation issues. Expected top-level areas include:

- `docs/` for design, permission, attribution, and technical records
- `source/` for authorized upstream inventories and conversion manifests
- `tools/` for deterministic import and validation tooling
- `mod/` for the distributable Gates of Hell project
- `tests/` for structural, content, and regression validation

Large binary assets should use the repository's approved large-file strategy rather than ordinary Git commits.

## Credits

- **WarFighter Modification - Total Overhaul**: approved source project and content library
- **Yuri**: primary WarFighter developer and permission grantor for the complete WarFighter mod and all included content
- **Additional WarFighter contributors**: credited where identifiable through the source inventory and original project records
- **Gates of WarFighter**: independent Gates of Hell adaptation, systems work, content integration, and strategic campaign implementation

## Legal and platform notice

This is a community-created mod project. It is not affiliated with or endorsed by Digitalmindsoft, Barbedwire Studios, Valve, or the owners of third-party intellectual property represented by source material. All applicable rights remain with their respective owners.
