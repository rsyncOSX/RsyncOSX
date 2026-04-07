
# RsyncUI

[![GitHub license](https://img.shields.io/github/license/rsyncOSX/RsyncUI)](https://github.com/rsyncOSX/RsyncUI/blob/main/Licence.MD)
![GitHub Releases](https://img.shields.io/github/downloads/rsyncosx/RsyncUI/v2.9.3/total)
[![GitHub issues](https://img.shields.io/github/issues/rsyncOSX/RsyncUI)](https://github.com/rsyncOSX/RsyncUI/issues)

This is [the repository for RsyncUI](https://github.com/rsyncOSX/RsyncUI), a SwiftUI based macOS application. RsyncUI is released for *macOS Sonoma and later*. RsyncUI is a GUI on the Apple macOS platform for the command line tool [rsync](https://github.com/WayneD/rsync). It is `rsync` which executes the synchronize data tasks. The GUI is *only* for organizing tasks, setting parameters to `rsync` and make it easier to use `rsync`.

| Homebrew | macOS versions |   Latest version   |
| ----------- |   ----------- | ----------- |
| `brew install --cask rsyncui`    | macOS Sonoma and later | v2.9.3 - [March 20, 2026](https://github.com/rsyncOSX/RsyncUI/releases) - in *active development* |
| |  | [documentation](https://rsyncui.netlify.app/docs/) and [changelog](https://rsyncui.netlify.app/blog/) |

If you find RsyncUI useful, I would appreciate it if you could consider giving me a star on [the repository](https://github.com/rsyncOSX/RsyncUI). Your support helps drive further development!

The [user documentation](https://rsyncui.netlify.app/docs/) is based upon a fork of the excellent Hugo based theme [Docsy](https://github.com/google/docsy). RsyncUI might be installed by Homebrew or by direct download. It is *signed* and *notarized* by Apple.

![](images/rsyncui.png)

---

# RawCull

[![GitHub license](https://img.shields.io/github/license/rsyncOSX/RawCull)](https://github.com/rsyncOSX/RawCull/blob/main/Licence.MD)

RawCull is a macOS app designed to help you quickly and efficiently cull large sets of Sony ARW A1 mkI and mkII raw photos. With a streamlined interface and powerful selection tools, RawCull makes it easy to review, compare, and select your best images.

## ARW body compatibility diagnostic

All 76 files in test, parsed successfully across EXIF, focus points, sharpness, and saliency, with one exception: the ILCE-7RM5 produced a saliency failure on 1 of its 3 files. The ILCE-1M2 dominates the dataset at 55 files (72% of total), and is also the only body tested across all three Sony RAW size variants (S/M/L). All files use compressed RAW, and every body achieves full-resolution L-size output — ranging from 12.4 MP (ILCE-1M2 S-crop) up to 60.2 MP on the ILCE-7RM5.

The two next bodies to focus on are the ILCE-7M5 and ILCE-7RM5. However, I am dependent on test ARW files provided to me to test properly before I officially conclude support for these two bodies as well. I am aware of an issue with the ILCE-7M5 and compressed ARWs.

| Camera Body | Files | EXIF | FocusPt | Sharpness | Saliency | RAW Types | Dimensions |
|---|---|---|---|---|---|---|---|
| ILCE-1 | 4 | 4/4 | 4/4 | 4/4 | 4/4 | Compressed | 8640 × 5760 (49.8 MP, L) |
| ILCE-1M2 | 55 | 55/55 | 55/55 | 55/55 | 55/55 | Compressed | 4320 × 2880 (12.4 MP, S), 5616 × 3744 (21.0 MP, M), 8640 × 5760 (49.8 MP, L) |
| ILCE-7M5 | 8 | 8/8 | 8/8 | 8/8 | 8/8 | Compressed | 7008 × 4672 (32.7 MP, L) |
| ILCE-7RM5 | 3 | 3/3 | 3/3 | 3/3 | 2/3 | Compressed | 9504 × 6336 (60.2 MP, L) |
| ILCE-9M3 | 3 | 3/3 | 3/3 | 3/3 | 3/3 | Compressed | 6000 × 4000 (24.0 MP, L) |
| MODEL-NAME | 3 | 3/3 | 3/3 | 3/3 | 3/3 | Compressed | 7008 × 4672 (32.7 MP, L) |
| **Total** | **76** | **76/76** | **76/76** | **76/76** | **75/76** | | |

RawCull is available for download on the [Apple App Store](https://apps.apple.com/no/app/rawcull/id6759362764?mt=12) or from the [GitHub Repository](https://github.com/rsyncOSX/RawCull/releases). It is possible that the GitHub version is released a day or two before the Apple App Store release due to the different release processes employed by each platform.

| macOS versions |   Latest version   |
|   ----------- | ----------- |
| macOS 26 Tahoe, **Apple Silicon** (M-series) only | v1.4.0  - April 7, 2026  - in *active development* |
|  | [documentation](https://rawcull.netlify.app/docs/) and [changelog](https://rawcull.netlify.app/blog/) |

![](images/rawcull.png)

