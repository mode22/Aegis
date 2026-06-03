# Update Manifest Documentation

## Purpose

Aegis releases use update manifests to communicate latest available versions and release metadata.

## Manifest Files

- `latest.json`: public JSON manifest for version distribution metadata
- `latest.yml`: update metadata manifest used by `electron-updater` compatible flows

## Contract Requirements

For each release:

1. Manifest version values must match the release tag.
2. Manifest links must point to published release assets.
3. Channel designation must be explicit.
4. Manifest files must be published alongside release assets.

## latest.json Minimum Fields

- `product`
- `channel`
- `latest_version`
- `release_date`
- `release_notes`
- `changelog`

## latest.yml Minimum Fields

- `version`
- `files`
- `path`
- `sha512`
- `releaseDate`

## latest.yml Example

```yaml
version: X.Y.Z
files:
  - url: Aegis-Setup-X.Y.Z.exe
    sha512: <BASE64_SHA512>
    size: <FILE_SIZE>
path: Aegis-Setup-X.Y.Z.exe
sha512: <BASE64_SHA512>
releaseDate: YYYY-MM-DDTHH:MM:SSZ
```

## NSIS Distribution Notes

When NSIS installers are distributed, the installer artifact referenced in `latest.yml` must be attached to the same GitHub Release.

