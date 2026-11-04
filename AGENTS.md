# Release hub maintenance

Follow the public contract in `docs/release-contract.md`. Track work in the
existing Hearts Mobile Project; current tasks are in `moztopia/hearts-mobile`.
Use an issue-linked `wip/{major}/{issue-number}-{slug}` branch and a PR to
`develop`. Each accepted hub-source PR advances `VERSION` and tags the exact
merge with that numeric version; APK component versions remain independent.

This repository is public. Keep application source, credentials, private keys,
test-user data and raw diagnostic logs out of it. Attach approved APKs and
checksums to GitHub Releases. Preserve all Android build reservations and
published artifacts; never silently replace a distributed build.

Report device verification honestly. Current scope is DemoHearts Android
development prereleases; never infer production approval or other-brand work.
