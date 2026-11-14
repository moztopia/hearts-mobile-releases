# Mobile artifact release contract

## Scope and identities

Current artifact: DemoHearts Android, application ID
`com.moztopia.hearts.demohearts`. APKs use the development-only identity created
under private mobile issue #358; never a production identity.

Public certificate SHA-256:
`9910970C0036EA6F0134438F82A50C3A7AD3113BA636073FD9BD25CA9832D662`.

This public repository stores guidance and public build metadata. Attach APKs
and checksums to Releases; never commit binaries, private source, user data,
keystores, passwords, access tokens, internal configuration or raw test logs.
Private-source URLs identify provenance without granting source access.

## Separate hub and application versions

`VERSION` and numeric tags such as `0.0.1` identify this repository's source
integrations. The initial baseline is `0.0.0`; each accepted `develop` PR
advances its patch exactly once and tags the exact merge. These numeric tags
are independent of every application/component version.

The Android application keeps the version from its selected hearts-mobile
numeric source tag. Its independent distributed Android build number never
resets when source versions change. Artifact release tags use
`demohearts-android-build-<number>`; release titles include the source version
and build number. An artifact tag points to this hub's metadata revision,
not the private application commit. The manifest separately records the
private application tag and full commit.

Asset names:

- `demohearts-<source-version>-build<number>.apk`
- `demohearts-<source-version>-build<number>.apk.sha256`
- `demohearts-<source-version>-build<number>.json`

One complete installable APK is supplied per build; its manifest declares the
architectures actually packaged. Do not substitute an incomplete split APK set.

## Reservation, approval and immutability

On14November2026 the owner selected `hearts+notify` and authorized automatic
DemoHearts Android development cuts from the private source repository's remote
`develop`. This supersedes the original manual-only trigger rule for that
configured target. Other targets and production publication remain separate.
The existing manual publisher can still serve explicitly selected work.

Each accepted source integration advances its numeric patch once and receives
an immutable tag at the exact merge. CI builds that source with the existing
development signer and the next permanent Android reservation. It first
publishes and anonymously verifies an immutable numbered build, then stages
those uniquely named assets in the rolling **hearts+notify** prerelease.
The stable slot tag is `demohearts-development-6865617274732b6e6f74696679`;
it points to public hub metadata, never private application source. Its current
notes change only after verification, and previous assets remain available.
A failed or stale cut cannot replace the previous current build. The workflow
cannot create credentials, broaden App permissions or change signing identity.

Reservation and immutable publication retain the allocator contract from #360:

1. Inspect all existing `demohearts-android-build-*` Git refs, including failed
   reservations and tags with no published Release.
2. Atomically create the next unused numbered tag ref at the selected hub
   revision. If another publisher won that number, refresh and try the next.
3. Persist the reservation before building. Never delete/reuse a failed number.
4. Build the exact selected application source commit with that Android number.
5. Verify artifact signature, package/version/build metadata, non-debuggable
   configuration, checksum, intended backend and relevant test results.
6. Publish a new release and assets under that reservation; never overwrite
   assets for an already distributed build or silently move its tag.

Counters are per application ID and Android signing/update line, not per
developer or selected source version. Reruns reserve another number. Concurrent
creation of the same tag must fail rather than distribute duplicate numbers.

For the first release the owner explicitly permitted publication as a development
**prerelease** before connected-phone testing. Clearly mark installation,
sign-in and in-place update checks as unverified; keep their acceptance open.
Static verification or a successful build does not establish phone behavior.

## Release manifest and notes

Use [release-notes-template.md](release-notes-template.md). Public metadata must
include application ID; visible version and Android build number; exact source
repository/tag/commit; hub revision/tag; SDK/toolchain and dependency provenance;
APK name/size/SHA-256; signing certificate SHA-256; min/target SDK and packaged
ABIs; backend URL/environment/availability; validation evidence; known defects
and explicitly untested cases. Never include private keys or credentials.

Published releases and assets must be downloadable without a GitHub account.
Verify the downloaded bytes match the locally checked file. Repository
maintainers need appropriate write access; public downloaders need no source
repository permissions. This does not promise worldwide device-installation
eligibility or bypass Android's installation policies.
