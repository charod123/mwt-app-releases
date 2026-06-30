# MWT App Releases

Public update channel for the MWT Android application.

The repository stores only update metadata. APK files must be uploaded as
GitHub Release assets and must never be committed directly to the repository.

## Release requirements

- Keep the Android application ID unchanged.
- Increment `build` for every release.
- Sign every APK with the same production signing key.
- Upload the APK to a GitHub Release.
- Calculate the APK SHA-256 checksum.
- Update `version.json` only after the Release asset is available.

The app must ignore a manifest when its `build` is not greater than the
installed build. For a newer build, `apk_url` and `sha256` must both be valid
before the app offers the update.

