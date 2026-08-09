# Gates of WarFighter

**Modern war, fought one province at a time.**

Gates of WarFighter is a standalone modern-warfare total conversion for **Call to Arms: Gates of Hell**. It combines a persistent strategic overmap campaign with real-time tactical battles using WarFighter models authorized by Yuri and additional source assets only where authorship and reuse permission have been verified.

## Project identity

Gates of WarFighter is being built as an independent Gates of Hell mod:

- No Code:X dependency
- No West81 dependency
- No WarFighter Workshop dependency at runtime
- No other content-mod dependency planned for the core experience
- WarFighter-derived assets are imported only where permission and provenance are documented
- Factions, rosters, research, campaign progression, AI integration, and strategic systems are rebuilt specifically for Gates of Hell

The strategic campaign is based on the overmap concept developed for Gates of Code:X, but this repository has its own technical foundation, content pipeline, release packaging, and acceptance process.

## Intended experience

Players will choose a modern nation, develop its military, research new capabilities, recruit authentic formations, expand across a persistent operational map, and personally command the battles that determine control of each region.

Planned pillars include:

1. Standalone installation and launch
2. Authorized WarFighter models and separately cleared supporting assets ported to Gates of Hell
3. Nation-specific rosters and research trees
4. Persistent strategic conquest over an operational map
5. Tactical battles driven by strategic state
6. Save/load integrity and deterministic content generation
7. Auditable asset provenance and contributor attribution

## Current status

**Pre-production / repository foundation.**

The first development gates are asset authorization documentation, source inventory, conversion feasibility, clean standalone boot, and one vertical-slice faction. Broad content import must not begin until the provenance and technical pipelines are defined.

See [the roadmap](docs/ROADMAP.md) and the repository issues for the ordered implementation plan.

## Asset permission and attribution

The project owner reports receiving express permission from **Yuri**, the primary WarFighter developer, to use all models authored by Yuri. That permission must not be assumed to cover textures, sounds, code, maps, animations, branding, or work authored by other contributors unless those rights are separately confirmed.

The working permission record and evidence requirements are maintained in [docs/ASSET_PERMISSION.md](docs/ASSET_PERMISSION.md). WarFighter-derived content must remain identifiable in the project inventory and credits. See [docs/ATTRIBUTION.md](docs/ATTRIBUTION.md).

Permission to use an asset does not imply ownership, permission to relicense it, or permission to remove original creator credits.

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

- **WarFighter Modification - Total Overhaul**: source project for approved porting work
- **Yuri**: primary WarFighter developer and permission grantor for models authored by Yuri
- Additional WarFighter contributors: to be identified and credited through the source inventory before their work is imported or publicly released
- **Gates of WarFighter**: independent Gates of Hell adaptation, systems work, content integration, and strategic campaign implementation

## Legal and platform notice

This is a community-created mod project. It is not affiliated with or endorsed by Digitalmindsoft, Barbedwire Studios, Valve, or the owners of third-party intellectual property represented by source material. All applicable rights remain with their respective owners.
