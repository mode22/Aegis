# Release and Versioning Policy

## Scope

This policy defines how Aegis public releases are versioned and published through this repository.

## Version Format

Releases use the following format:

- `MAJOR.MINOR.PATCH`

Tag format:

- `vMAJOR.MINOR.PATCH`

## Release Channels

- `stable` for production-intended public releases
- `prerelease` for validation and early evaluation builds

## Release Requirements

Each release must include:

- Release notes
- Updated changelog entries
- Update manifests (`latest.json` and `latest.yml` where applicable)
- Integrity verification artifacts

## Release Quality Gate

Before publishing:

1. Confirm release version consistency across artifacts.
2. Confirm manifest values match release tag.
3. Confirm integrity metadata is present.
4. Confirm documentation links are valid.

## Deprecation and Replacement

When a release is replaced or withdrawn, release notes must be updated with clear replacement guidance.

