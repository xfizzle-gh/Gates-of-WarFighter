# Asset Permission Record

## Purpose

This document records the project's current understanding of permission to reuse material from **WarFighter Modification - Total Overhaul**. It is a project-control record, not a substitute for the original permission conversation or legal advice.

## Current recorded permission

- **Source project:** WarFighter Modification - Total Overhaul
- **Permission grantor:** Yuri, identified by the project owner as the primary WarFighter developer
- **Permission recipient:** Gates of WarFighter project owner
- **Recorded by:** Repository owner
- **Record date:** 2026-08-09
- **Permission reported:** Express permission to use all models authored by Yuri in Gates of WarFighter
- **Intended use:** Port authorized models into a standalone Call to Arms: Gates of Hell mod and use them in newly built factions, rosters, research trees, tactical content, and strategic campaign systems

## Scope boundaries

The recorded permission must not be interpreted more broadly than the grant actually supports.

Unless separately confirmed, the following remain **unverified**:

- Textures, materials, normal maps, and other image files
- Models authored or co-authored by anyone other than Yuri
- Animations and rigging authored by others
- Sounds, music, voice work, maps, scripts, configuration, UI, logos, and branding
- Assets incorporated into WarFighter from other games, mods, marketplaces, or creators
- Permission to relicense, sell, sublicense, or claim ownership of source assets

A model may also depend on textures, materials, animations, or source files whose rights differ from the model itself. Every dependency must be inventoried before the asset is accepted into a public build.

## Evidence requirement

Before broad asset import begins, the project owner should preserve the original permission evidence outside the repository and, where appropriate, add a redacted or approved copy under `docs/permission-evidence/`.

The evidence record should capture:

1. Yuri's account identity or other reliable identifier
2. The date and platform of the conversation
3. The exact permission language
4. Whether the permission covers modification, redistribution, and public Workshop release
5. Whether attribution wording was requested
6. Whether textures and other model dependencies are included
7. Whether Yuri is authorized to grant permission for every included asset

Do not publish private messages, personal information, or screenshots without the participants' consent.

## Asset acceptance rule

No WarFighter-derived file may enter a distributable build until its manifest entry records:

- Source path and source version
- Asset type
- Author or best-known author
- Permission basis
- Required attribution
- Dependencies
- Conversion steps
- Destination path
- File hash before and after conversion
- Reviewer and acceptance status

Unknown authorship or unclear permission is a blocking state, not an invitation to infer approval.

## Revocation or dispute handling

If a creator disputes use of an asset, that asset and its derivatives must be quarantined from release while the claim is reviewed. The project should preserve history and evidence, avoid public argument in asset files or commit messages, and replace or remove content when permission cannot be established.

## Confirmation checklist

- [ ] Original permission evidence preserved
- [ ] Yuri's exact authorship scope identified
- [ ] Modification permission confirmed
- [ ] Redistribution in this repository confirmed
- [ ] Steam Workshop redistribution confirmed
- [ ] Texture and material rights confirmed separately
- [ ] Third-party source assets identified
- [ ] Attribution wording approved or documented
- [ ] Asset manifest schema established
