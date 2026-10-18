# Zag Store Release Policy

## Development

Zag Store 1.0.0 Builds 1–4 are prelaunch test builds.

Build 4 is the current Beta v2 baseline.

Development builds do not establish the public Stable version history.

Existing signed manifests, IPA assets, and checksums must remain unchanged.

## Public Launch

The first official Stable release is reserved as:

Zag Store 1.0.0 (Build 1)

No Stable manifest will be published until the final production IPA is signed, verified, and approved.

## Authenticated Updates

Beta v2 uses authenticated release metadata with signature verification, SHA-256 validation, expiration, and rollback protection.

Stable and Nightly must be validated independently before activation.

## Migration

Existing development installations may have higher build numbers than the first public release.

Migration must be explicitly tested. Never bypass signing, identity, or rollback protections.

Verify application data and Keychain continuity before releasing a migration procedure.
