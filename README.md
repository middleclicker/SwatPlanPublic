# SwatPlan Public

The public website, downloads, development changelog, support information, and privacy policy for SwatPlan.

- Website: https://middleclicker.github.io/SwatPlanPublic/
- Downloads: https://middleclicker.github.io/SwatPlanPublic/#download
- Changelog: https://middleclicker.github.io/SwatPlanPublic/#changelog
- Support: https://middleclicker.github.io/SwatPlanPublic/#support
- Privacy policy: https://middleclicker.github.io/SwatPlanPublic/#privacy
- iPhone App Store listing: https://apps.apple.com/us/app/swatplan/id6808754828

## Updating the website

This is a static website. Edit `index.html` and `styles.css`, then push to `main` to publish through GitHub Pages. Preview locally with `python3 -m http.server 4173`.

Keep the public App Store release separate from development updates. As of October 1, 2026, the App Store listing is iPhone-only at version 1.0.1; iPad support and newer features appear in development builds.

## Mac preview

`downloads/SwatPlan-Mac-1.2.3.zip` contains version 1.2.3 (build 7), copied from the app repository's signed Mac package. It is a universal Apple silicon/Intel Mac Catalyst build requiring macOS 15 or later.

**This is an Apple Development build for registered test Macs, not a notarized release for general distribution.** Preserve this limitation next to the download button until a public distribution build replaces it.

For a new preview, run `Scripts/package_mac.sh` in the private app repository, verify the signature and provisioning, copy the versioned ZIP into `downloads/`, and update the download filename, version, size, and notes. Generate the checksum from this repository root:

```sh
shasum -a 256 downloads/SwatPlan-Mac-1.2.3.zip > downloads/SwatPlan-Mac-1.2.3.zip.sha256
```

Do not add private app source, tokens, sync documents, or local planner data to this public repository.
