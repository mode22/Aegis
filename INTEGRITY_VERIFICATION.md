# Integrity Verification Guidance

## Purpose

This document defines how integrity metadata is handled for Aegis release artifacts.

## Required Integrity Artifacts

Each release should publish:

- `SHA256SUMS` file for release assets
- `latest.yml` integrity fields (`sha512`)
- Optional detached signature files when signing is enabled

## Verification Expectations

Consumers should verify checksums before applying updates.

Maintainers must ensure checksum files correspond exactly to uploaded release assets.

## Publication Rules

1. Generate integrity artifacts from final release binaries.
2. Publish integrity artifacts in the same GitHub Release.
3. Ensure release notes reference integrity artifacts.

## Future Code-Signing Plan

Before enabling signing in production distribution:

- Define signing key ownership and access control.
- Define signing step ownership in the release workflow.
- Define secret storage and rotation policy.
- Define signature verification guidance for consumers.

