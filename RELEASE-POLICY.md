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

## Owner exceptions

### Beta 4 replacement (November 2026)

The owner authorised one exception to "Existing signed manifests, IPA assets,
and checksums must remain unchanged":

- **Withdrawn:** release `v1.0.0-beta.4`, built from Zag Store
  `c5b517b441a5687dedc8f3e2d46dc35f0e3787f4`, with assets
  `ZagStore-1.0.0-beta.4.ipa` (SHA-256
  `1acb00079417473ab5384179586d254d289384d8ae40aa510029629083820ad3`,
  59,506,194 bytes) and its `.sha256` file, is deleted together with its tag.
  It was withdrawn after publication because of a regression in the in-app
  update's completion step.
- **Replacement:** a new `v1.0.0-beta.4` release, still 1.0.0 build 4, built
  from `a8cdcbb9d99c462ee4fce44404f5bf132e09ece4`. Its IPA,
  `ZagStore-1.0.0-beta.4-a8cdcbb9.ipa`, has SHA-256
  `358a546442eb1a150c843515e40e5f549204e2e81d6f2f23bc0683b84f2e810a`
  (59,535,709 bytes).
- **Metadata:** signed Beta v2 sequence 8 names the replacement. Sequence 7,
  which named the withdrawn IPA, is kept as
  `releases/v2/beta-sequence-7-backup.json`. Sequences never decrease.

This exception covers only the release, tag and assets above. Every other
release, asset, checksum and signed manifest remains unchanged, and later
corrections are published as a new build.
