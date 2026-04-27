# RsyncUI
[![GitHub license](https://img.shields.io/github/license/rsyncOSX/RsyncUI)](https://github.com/rsyncOSX/RsyncUI/blob/main/Licence.MD)
![GitHub Releases](https://img.shields.io/github/downloads/rsyncosx/RsyncUI/v2.9.3/total)
[![GitHub issues](https://img.shields.io/github/issues/rsyncOSX/RsyncUI)](https://github.com/rsyncOSX/RsyncUI/issues)

[RsyncUI](https://github.com/rsyncOSX/RsyncUI) is a SwiftUI macOS GUI for the command line tool [rsync](https://github.com/WayneD/rsync). It handles task organisation, parameter configuration, and scheduling — `rsync` does the actual work of synchronising your data. Requires *macOS Sonoma or later*.

| Homebrew | macOS | Latest version |
| --- | --- | --- |
| `brew install --cask rsyncui` | macOS Sonoma and later | v2.9.3 — [March 20, 2026](https://github.com/rsyncOSX/RsyncUI/releases) — *active development* |
| | | [Documentation](https://rsyncui.netlify.app/docs/) · [Release notes](https://rsyncui.netlify.app/blog/) |

RsyncUI can be installed via Homebrew or direct download. It is *signed* and *notarized* by Apple. The [user documentation](https://rsyncui.netlify.app/docs/) is built on a fork of the Hugo-based [Docsy](https://github.com/google/docsy) theme.

If RsyncUI is useful to you, a ⭐ on [the repository](https://github.com/rsyncOSX/RsyncUI) is always appreciated!

![](images/rsyncui.png)

---

# RawCull
[![GitHub license](https://img.shields.io/github/license/rsyncOSX/RawCull)](https://github.com/rsyncOSX/RawCull/blob/main/Licence.MD)

RawCull is a macOS photo review and culling application for Sony ARW RAW files, built exclusively for Apple Silicon. It combines a streamlined interface with GPU-accelerated analysis — including EXIF extraction, focus point detection, sharpness scoring, and saliency — to help you quickly identify your best shots.

## Sony ARW compatibility

| Camera Body  | EXIF | FocusPt | Sharpness | Saliency | RAW Types | Dimensions |
|---|---|---|---|---|---|---|
| ILCE-1M2  |  ✅  |  ✅  |  ✅  |  ✅  | Compressed | 4320 × 2880 (12.4 MP, S), 5616 × 3744 (21.0 MP, M), 8640 × 5760 (49.8 MP, L) |
| ILCE-1   |  ✅  |  ✅  | ✅  | ✅  | Compressed | 8640 × 5760 (49.8 MP, L) |
| ILCE-7M5  |  ✅  |  ✅  |  ✅  |  ✅  | Compressed | 7008 × 4672 (32.7 MP, L) |
| ILCE-7RM5  |  ✅  |  ✅  |  ✅  |  ✅  | Compressed | 9504 × 6336 (60.2 MP, L) |
| ILCE-9M3 |  ✅  |  ✅  |  ✅  | ✅  | Compressed | 6000 × 4000 (24.0 MP, L) |

## Nikon NEF body compatibility (experimental)

Nikon support targets current Z-series bodies. AF-point extraction uses the `AFInfo2` tag (0x00B7) with the `0300`+ layout common to Z9, Z8, Z7, and Z6 families; older DSLRs fall through and currently return `nil` for focus points while EXIF, thumbnail extraction, and sharpness scoring still work. Size-class thresholds for L/M/S are tuned per body (~45 MP for Z9/Z8/Z7/D850, ~24 MP for Z6).

| Camera Body | EXIF | FocusPt | Sharpness | Saliency | RAW Types | Dimensions |
|---|---|---|---|---|---|---|
| Z9 | ✅ | ❌ | ✅ | ✅ | Compressed | ~8256 × 5504 (45.4 MP, L) |
| Z8 | ✅ | ❌ | ✅ | ✅ | Compressed | ~8256 × 5504 (45.7 MP, L) |
| Z7 / Z7 II | ✅ | ❌ | ✅ | ✅ | Compressed | ~8256 × 5504 (45.7 MP, L) |
| Z6 / Z6 II / Zf | ✅ | ❌ | ✅ | ✅ | Compressed | ~6048 × 4024 (24.3–24.5 MP, L) |


| macOS | Latest version |
| --- | --- |
| macOS Sequoia, **Apple Silicon** (M-series) only | v1.6.5 — April 26, 2026 — *active development* |
| | [Documentation](https://rawcull.netlify.app/docs/) · [Release notes](https://rawcull.netlify.app/blog/) |

RawCull is available on the [Apple App Store](https://apps.apple.com/no/app/rawcull/id6759362764?mt=12) and via [GitHub Releases](https://github.com/rsyncOSX/RawCull/releases).
![](images/rawcull.png)
