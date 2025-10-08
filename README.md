# Curo Calculator Binary Distributions

This repository hosts binary distribution files for the Curo Calculator app, a proprietary calculator built with Flutter for performing advanced instalment credit financial calculations, including loan, lease, and hire purchase repayments and interest rates. It's designed for personal users and finance professionals to simplify complex financial computations.

The distributions include:
- **Linux Desktop App**: Available via Flatpak on Flathub, bundled as `curocalc-[version]-linux-x86_64.tar.gz`.
- **Android App**: Self-signed APK for sideloading, available as `curocalc-[version]-android.apk`.

## Features
- Perform advanced financial calculations for loans, leases, and hire purchase agreements.
- User-friendly interface built with Flutter for cross-platform consistency.
- Powered by the open-source [Curo library](https://github.com/andrewmurphy353/curo) for reliable calculations.

## Metadata
- **Homepage**: https://curocalc.app
- **License**:
  - Repository metadata (Flatpak manifest `app.curocalc.calculator.yml`, `app.curocalc.calculator.desktop`, `app.curocalc.calculator.metainfo.xml`): MIT License (see [LICENSE](LICENSE)).
  - Icon (`app.curocalc.calculator.svg`) and Curo Calculator app binaries (Linux tarball and Android APK): Proprietary (end-user license terms at https://curocalc.app/terms).
  - Underlying calculation library: MIT License ([Curo library](https://github.com/andrewmurphy353/curo)).
- **Releases**: Prebuilt binaries for Linux (built on Debian GNU/Linux 12 (bookworm), Flutter 3.35.4) and Android (built with Flutter 3.35.4). Download the latest from the [Releases](https://github.com/andrewmurphy353/curo_app_bin/releases) page.
- **Support**: Report technical issues at https://github.com/andrewmurphy353/curo_app_bin/issues or contact curocalculator@gmail.com.
- **Privacy Policy**: https://curocalc.app/privacy

## Installation

### Linux (Flatpak)
Install [Curo Calculator](https://flathub.org/en/apps/app.curocalc.calculator) via Flathub:
```
flatpak install flathub app.curocalc.calculator
```

For manual installation or testing:
1. Ensure Flatpak is installed on your system.
2. Download and use the provided Flatpak manifest (`app.curocalc.calculator.yml`) from the [Releases](https://github.com/andrewmurphy353/curo_app_bin/releases) page to build and install locally:
   ```
   flatpak-builder --install build-dir app.curocalc.calculator.yml
   ```

### Android (APK)
1. Download `curocalc-[version]-android.apk` from the [Releases](https://github.com/andrewmurphy353/curo_app_bin/releases) page.
2. Enable "Install from unknown sources" in your Android device settings.
3. Open the APK file to install.
4. **Note**: This is a self-signed APK for sideloading. For production use, consider Google Play distribution or RuStore (see https://curocalc.app for links).

## About
Curo Calculator is built on the open-source [Curo library](https://github.com/andrewmurphy353/curo), a feature-rich Dart library for instalment credit calculations, released under the MIT License. While the Curo Calculator app itself is proprietary, the core calculation engine is open-source, reflecting our commitment to the open-source community.

The source code for the Curo Calculator app is proprietary and not available in this repository. This repo provides the binaries, Flatpak manifest, and assets for Flathub integration.

## Flathub Compliance
This repository is structured to meet Flathub requirements:
- The Flatpak manifest (`app.curocalc.calculator.yml`) downloads and integrates the proprietary binary tarball.
- `app.curocalc.calculator.metainfo.xml` specifies `project_license` as `LicenseRef-proprietary` with a link to terms.
- Metadata files (`app.curocalc.calculator.yml`, `app.curocalc.calculator.desktop`, `app.curocalc.calculator.metainfo.xml`) are provided under MIT; the icon (`app.curocalc.calculator.svg`) is proprietary.
- Builds use Flathub-hosted runtimes with no end-of-life dependencies.
- OARS content rating: Safe for general audiences (no violence, etc.).
- Screenshots: Included in `app.curocalc.calculator.metainfo.xml` with direct URLs.
