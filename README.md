# Anchor Point — iOS

Native iOS wrapper around the [anchorestates.co](https://anchorestates.co) PWA. Ships to the Apple App Store via Codemagic.

## Build pipeline

1. `xcodegen` regenerates `AnchorPoint.xcodeproj` from `project.yml` at build time — no `.xcodeproj` is committed.
2. Codemagic (`codemagic.yaml`) fetches signing, runs `xcodegen`, builds the `.ipa`, and uploads to App Store Connect.
3. TestFlight is the default publish target; flip the `submit_to_app_store` flag in `codemagic.yaml` when ready for review.

## Local prerequisites (for devs poking at it)

- macOS + Xcode 15+
- `brew install xcodegen`
- Run `xcodegen generate` to produce `AnchorPoint.xcodeproj`, then open that in Xcode.

## Bundle info

- Bundle ID: `co.anchorestates`
- Display name: Anchor Point
- Min iOS: 15.0
- Device family: iPhone + iPad

## Icons

`AnchorPoint/Assets.xcassets/AppIcon.appiconset/AppIcon-1024.png` is currently a placeholder lettermark. Replace with the real 1024×1024 brand icon (8-bit RGB, no alpha) before App Store submission.
