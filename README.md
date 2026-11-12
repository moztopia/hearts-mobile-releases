# Hearts mobile releases

Public downloads and release notes for Hearts mobile applications.
The current delivery is **DemoHearts for Android**, signed with a development-only
key for testing. These builds must never be used as production releases.

**[Browse available downloads](https://github.com/moztopia/hearts-mobile-releases/releases)**

**[Download DemoHearts 0.0.64 — Android build 10 (APK)](https://github.com/moztopia/hearts-mobile-releases/releases/download/demohearts-android-build-10/demohearts-0.0.64-build10.apk)**

This development prerelease is signed and its package metadata and checksum
have been verified. All 845 host checks, source analysis and SDK dependency
verification passed. Physical installation, launch, sign-in, onboarding and
in-place update remain unverified for this exact APK. Earlier phone checks do
not establish acceptance of this build. Use test data only. Read the
[release notes and checksums](https://github.com/moztopia/hearts-mobile-releases/releases/tag/demohearts-android-build-10)
before installing. Android 7.0 (API 24) or later is required.

The repository contains downloads, release guidance and metadata, not application
source code or signing credentials. Build tags 1, 2, 5, 6, 7 and 9 reserve failed attempts;
they have no APK. Use the download link above or the Releases page, not source
archives from the Tags page.

Build 10 includes refined Browse cards with a subtle photo fade, compact
three-column actions and improved long-name/online-presence handling. Profile
settings have clearer sections; the current Profile cover cannot be deleted.
Onboarding refinements and silent best-effort logout cleanup are included,
along with SDK 0.1.15. Your searches and the previous localized controls remain.

Automated checks do not establish full phone acceptance. Interface review,
sign-in, onboarding and in-place update remain open for this build. Live Google
Maps activation and optional voice introductions remain unavailable. Provider
sign-in has not been reverified for this build.

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
