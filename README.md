# Hearts mobile releases

Public downloads and release notes for Hearts mobile applications. Current delivery
is **DemoHearts for Android**, signed with the existing development-only key.
Use test accounts/data; these APKs are not production releases.

**[Download the latest DemoHearts APK — hearts+notify](https://github.com/moztopia/hearts-mobile-releases/releases/tag/demohearts-development-6865617274732b6e6f74696679)**

Open that channel and download the APK filename identified in its current notes.
Older uniquely named assets remain available for rollback/history; they are not
necessarily the current cut. Numeric source versions and Android build numbers
remain separate from the persistent owner-selected name **hearts+notify**.

Remote develop integrations automatically build only DemoHearts Android in the
pinned container. The workflow verifies an immutable numbered build and anonymous
downloads before switching the channel's current notes. Failed/stale cuts preserve
its previous working payload. See the [release contract](docs/release-contract.md).

## Verified cut — 14 November 2026

[DemoHearts 0.0.77, Android build 24](https://github.com/moztopia/hearts-mobile-releases/releases/tag/demohearts-android-build-24)
is the first verified automatic named cut. It includes the main-tab notification
bell, authorized people/event cards and corrected conversation/sign-in recovery.
The candidate passes935 app/appearance/manual-publisher checks, source analysis
and reviewed SDK0.1.17 verification. The hosted workflow also passes release
analysis, signing/package checks and public asset verification. Independent
anonymous downloads from both release locations match their checksums.

- Source tag: `0.0.77`; exact private source commit:
  `983525ac9e9ae6f08ed12314a9580fc53113419c`.
- APK SHA-256: `23936d98324e0ce6e96021b158c3b9e9209cc7ae8d99a45aec7c344cfdce88b0`.
- Android7.0/API24 or later; packaged ABIs: arm64-v8a,armeabi-v7a,x86_64.
- Application ID: `com.moztopia.hearts.demohearts`; existing development signing
  identity is preserved. The manifest records its public certificate fingerprint.

A private candidate with matching app/native source and catalog content was
checked on OPPO CPH2237/Android13 for bells/history/Back, people cards, unavailable
feedback, retained drafts, cold-process/sign-in resume and owner-confirmed tone
and short/light haptic. Those dated checks do not establish installation or full
physical acceptance of this newly published APK and its resolved dependencies.
No phone reinstall was performed during publication. Fresh installation,
onboarding and an upgrade between distributed APKs remain unverified here.

Known limitations: OPPO shows a notification dot when Number or dot is enabled;
numbered DemoHearts icon badges remain unresolved. Physical iPhone review and
APNs are pending; no iPhone artifact is included. Other new-candidate native
categories/themes/auth variants remain pending. Live Google Maps activation and
optional voice introductions also remain unavailable. Read the channel notes.
The developer backend/server/tunnel must be available for online app features.

Earlier numbered downloads remain unchanged. The12November0.0.64/build10 receipt
records an in-place same-certificate debug-to-release update, two cold launches
and retained session/settings on the OPPO; it does not certify this new APK.

## Install DemoHearts on Android

1. Open the downloads link above on your Android phone.
2. Open the desired **DemoHearts Android** release and read its known limitations.
3. Under **Assets**, download the file ending in `.apk`. The automatically
   generated source ZIP/tar files are not the application.
4. Open the downloaded APK. Android may ask you to permit your browser or file
   manager to install applications from that source. Follow the device's prompts
   and confirm installation. Managed-device restrictions and prompts vary.
5. Launch DemoHearts. Use a test account and disposable test data.

See [Android's installation guidance](https://developer.android.com/distribute/marketing-tools/alternative-distribution).
Do not disable device protections to work around a failed installation; report
the exact error to the project maintainer.

## Update an existing installation

Download the newer APK and install it over the existing app. Its Android build
number must be higher and its signing identity compatible. Publication does not
automatically update your phone. Never uninstall or clear application data just
to get an update installed without first agreeing how to preserve that data.

Configured DemoHearts debug builds and these distributed test APKs now use the
same approved development signing certificate. Compatibility depends on the
package, certificate and Android build number, not debug/release mode. An older
installation signed with a different certificate cannot update in place.
Contact the maintainer if Android rejects an update; never uninstall or clear
data implicitly.

## Test service availability

Initial DemoHearts prereleases use the developer test backend at
`https://bruce-demohearts.moztopia.com`. That service depends on the developer's
local server and Cloudflare tunnel being available. An APK download remains
available when that backend is stopped, but sign-in and online app features
will not work. The APK is not a server deployment. Use coordinated test sessions.

## Versions and verification

The visible application version identifies the selected application source
release. The Android build number identifies a particular distributed build.
The first available APK, `demohearts-0.0.20-build3.apk`, is application version
`0.0.20`, Android build `3`.

Each APK release includes release notes, a SHA-256 checksum and a release
manifest describing its exact source version/commit, build number, certificate,
build provenance, supported devices, backend and outstanding checks. Keep older
downloads available for history; installing an older build is not an ordinary
supported update. Source links may require maintainer access to the private
application repository.

The repository's `VERSION` describes these release-hub documents and tooling;
it is independent of the app version shown on your phone. See the
[release contract](docs/release-contract.md) for maintainer details.

iPhone installation links may be added by separately authorized work. No iPhone
build or other brand is included in the current Android delivery.
