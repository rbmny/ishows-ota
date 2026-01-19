# ishows OTA Distribution

Over-The-Air (OTA) distribution for the ishows iOS app.

## How It Works

This repository hosts Ad Hoc builds that can be installed directly on registered iOS devices via Safari.

**Build artifacts are automatically deployed by the `build-adhoc.sh` script.**

## Installation

1. Open Safari on your iOS device
2. Visit: https://rbmny.github.io/ishows-ota
3. Tap "Install App"

Your device must be registered in the Ad Hoc provisioning profile.

## Files

- `ishows.ipa` - The iOS app package
- `manifest.plist` - OTA installation manifest
- `index.html` - Installation page

## Building

Builds are created using:

```bash
cd /path/to/ishows
./scripts/build-adhoc.sh
```

The script automatically:
- Increments build number
- Archives and exports the IPA
- Generates the manifest
- Commits and pushes to this repository
- GitHub Pages deploys within 1-2 minutes
