# Contributing to Gates of WarFighter

## Before contributing

Read:

- `README.md`
- `docs/ASSET_PERMISSION.md`
- `docs/ATTRIBUTION.md`
- `docs/DEVELOPMENT_PRINCIPLES.md`
- `docs/ROADMAP.md`

Do not submit WarFighter-derived files unless the relevant issue explicitly authorizes that asset slice and the required provenance records are included.

## Issue-first workflow

Foundational and asset-import work must begin from an approved issue that defines:

- Scope
- Dependencies
- Source authority
- Permission status
- Expected generated and handwritten files
- Tests and native acceptance evidence
- Explicit exclusions

Do not broaden a pull request because nearby cleanup appears convenient.

## Branches and pull requests

Use a descriptive branch name, preferably tied to the issue or gate. Open pull requests as drafts unless the issue explicitly permits otherwise.

A pull request should include:

1. The issue and gate it serves
2. Exact scope and exclusions
3. Changed-file summary
4. Source and provenance changes
5. Generated-output explanation
6. Tests actually executed
7. Native-game checks actually performed
8. Known limitations and unresolved risks
9. Exact head commit submitted for review

Foundational pull requests should receive independent review before merge.

## Asset submissions

Every imported or converted asset must have a manifest record. At minimum, include:

- Upstream source identifier and path
- Original author or best-known author
- Permission evidence reference
- Required dependencies
- Input checksum
- Conversion recipe and tool version
- Destination path
- Output checksum
- Required attribution
- Release-eligibility status

Unknown or mixed authorship must be resolved before the asset enters a public release branch.

Do not commit private permission conversations, personal information, or unapproved screenshots to the public repository.

## Generated content

Generated files must be produced by committed tooling and configuration. A contributor must not hand-edit generated output unless the generator and source authority are updated so the result remains reproducible.

Generation should fail rather than silently omit missing, ambiguous, or unauthorized dependencies.

## Testing

Use the narrowest useful checks while developing, then execute the issue's full acceptance set before requesting review.

Evidence should distinguish:

- Structural or static validation
- Conversion validation
- Automated tests
- Headless game checks
- Native Gates of Hell checks
- Manual visual inspection

Never report a check as passed when it was not executed on the exact pull-request head.

## Commit hygiene

- Keep commits intentional and reviewable
- Avoid unrelated formatting or file churn
- Do not commit local Workshop installations, caches, logs, save files, or private source archives
- Do not force-push an accepted review head without a documented reason and a fresh review request
- Do not merge around unresolved blocking findings

## Attribution corrections and disputes

Report missing credits or disputed asset use through a repository issue without publishing private evidence. Maintainers should quarantine affected release content while authorship and permission are reviewed.
