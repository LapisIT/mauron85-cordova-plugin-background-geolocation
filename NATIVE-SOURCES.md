# Native source provenance

The native sources under `ios/common` and `android/common` are vendored into
this repository so GitHub source archives and npm installations include them
without fetching Git submodules. Keep these paths unchanged: `plugin.xml`
references them directly.

## iOS

- Original upstream: https://github.com/mauron85/background-geolocation-ios
- Imported fork: https://github.com/LapisIT/mauron85-background-geolocation-ios
- Imported commit: `4fb70363c4f24f1dc6f022dcacf5ac7219f9208b`
- Includes removal of `#import <netinet6/in6.h>` from
  `BackgroundGeolocation/Reachability.m`.
- Licence: `ios/common/LICENSE`; retain existing source copyright notices.

## Android

- Upstream: https://github.com/mauron85/background-geolocation-android
- Imported commit: `2693e07587eea08746004bd3e72dde276b04b4d2`
- Licence: `android/common/LICENSE`; retain existing source copyright notices.

## Updating native sources

Import future native changes as ordinary files in these directories. Review
the source changes and update the imported commit IDs above in the same commit.
Preserve this fork's iOS import removal when updating from upstream.
