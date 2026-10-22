# Pix — Android TV releases

This public repository distributes **signed Pix APK releases only**. The application source code remains in the separate private `donlums/pix` repository.

Once the stable signing key and GitHub Actions secrets are configured in the private repository, publishing a tagged release will attach:

- `Pix.apk` — the signed Android TV / Google TV installer
- `latest.json` — version number, direct APK URL, SHA-256 checksum, and release notes

Pix checks for updates using:

`https://github.com/donlums/pix-releases/releases/latest/download/latest.json`

If a newer version exists, Pix offers to download a checksum-verified APK and opens Android's installer. Android may require the user to approve app installs and updates; **silent installation is not supported**.

**Not live yet:** Creating this repository is only the first step. A stable private signing key and a scoped repository publishing token must be configured before the signed release workflow can publish assets.

The public repo is not the place to upload a keystore, access tokens, signing passwords, source code, or private add-on configuration.
