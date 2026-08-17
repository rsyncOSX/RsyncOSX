# macOS apps by Thomas (rsyncOSX)

Native macOS applications for file synchronization, photo culling, and private on-device image search. All four (five) applications are actively developed, and their core processing stays on your Mac.

| Application | Purpose | Requirements |
| --- | --- | --- |
| [RsyncUI](#rsyncui) | Graphical file synchronization with `rsync` | macOS Sonoma and later |
| [RawCull](#rawcull) | GPU-accelerated Sony RAW photo culling | Apple Silicon, macOS Tahoe and later, version 2.3.5 is the latest on macOS Tahoe |
| [RawCull (AI)](#rawcull) | AI-assisted Sony RAW photo culling | Apple Silicon, macOS Golden Gate beta, version 3.0.0 is next version and will only run on macOS Golden Gate |
| [RawCullFB](#rawcullfb) | Private semantic image search using local AI | Apple Silicon, macOS Golden Gate beta |
| [GitBranchStatus](https://github.com/rsyncOSX/GitHubLocalRemote) | small app to display status local vs GitHub repository  | Apple Silicon, macOS Tahoe and later |

About Sandboxing and security, see last on page.

---

## RsyncUI

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/rsyncOSX/RsyncUI/blob/main/Licence.MD)
![RsyncUI v3.0.3 downloads](https://img.shields.io/github/downloads/rsyncosx/RsyncUI/v3.0.3/total)
![RsyncUI v3.0.2 downloads](https://img.shields.io/github/downloads/rsyncosx/RsyncUI/v3.0.2/total)

A native SwiftUI interface for [`rsync`](https://github.com/WayneD/rsync) that makes synchronization tasks easier to configure, organize, and schedule. RsyncUI configures and runs `rsync`; all file synchronization is performed by `rsync` itself.

[Download](https://github.com/rsyncOSX/RsyncUI/releases) · [Documentation](https://rsyncui.netlify.app/docs/) · [Release notes](https://rsyncui.netlify.app/blog/) · [Report an issue](https://github.com/rsyncOSX/RsyncUI/issues)

```shell
brew install --cask rsyncui
```

**Requires macOS Sonoma or later.** The latest release is [v3.0.3](https://github.com/rsyncOSX/RsyncUI/releases), released August 7, 2026. RsyncUI is signed and notarized by Apple.

![RsyncUI synchronization interface](images/rsyncui.png)

---

## RawCull

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/rsyncOSX/RawCull/blob/main/Licence.MD)

A fast, native photo-culling application for Sony ARW files. RawCull uses GPU-accelerated analysis—including EXIF extraction, focus-point detection, sharpness scoring, and visual saliency—to help you identify your strongest photographs.

[Download from the Mac App Store](https://apps.apple.com/no/app/rawcull/id6759362764?mt=12) · [GitHub releases](https://github.com/rsyncOSX/RawCull/releases) · [Download RawCull (AI) v3.0.0 beta](https://github.com/rsyncOSX/RawCull/releases/tag/v3.0.0) · [Documentation](https://rawcull.netlify.app/docs/) · [Release notes](https://rawcull.netlify.app/blog/)

**Requires Apple Silicon.** The current release, v2.3.5, supports macOS Tahoe and later. The [RawCull (AI) v3.0.0 beta](https://github.com/rsyncOSX/RawCull/releases/tag/v3.0.0) with AI-powered features is available for macOS Golden Gate beta. See the [documentation](https://rawcull.netlify.app/docs/) for supported Sony full-frame camera bodies.

![RawCull photo review interface](images/rawcull.png)

---

## RawCullFB

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/rsyncOSX/RawCullFB/blob/main/Licence.MD)

A private, on-device photo browser with natural-language search. RawCullFB uses local CLIP indexing to search JPEG, PNG, HEIC/HEIF, TIFF, and Sony ARW files—without uploading your photographs. Model inference, image embeddings, and search all stay on your Mac.

[Download](https://github.com/rsyncOSX/RawCullFB/releases)

**Requires Apple Silicon and macOS Golden Gate beta.** The latest release is [v2.4.1](https://github.com/rsyncOSX/RawCullFB/releases), released August 16, 2026. RawCullFB is sandboxed, signed, and notarized by Apple.

![RawCullFB semantic image search](images/rawcullfb.png)

---

If these applications are useful to you, consider starring their repositories. Feedback and issue reports are always welcome.

## Sandboxing, signing, and notarization

RsyncUI is not Sandboxed, but signed and notarized. RawCull and RawCullFB are Sandboxed, signed and notarized.

- **App Sandbox:** Both RawCullFB and its model-downloader extension run with the App Sandbox and Hardened Runtime enabled. The main app receives read/write access only to folders explicitly selected by the user and preserves that access with security-scoped bookmarks. The app and extension share model assets through their declared App Group. Sandboxing limits the files and system resources that compromised or defective code could reach; it does not establish who published the app.
- **Code signing:** Release exports use an Apple-issued **Developer ID Application** identity. The release workflow verifies the signatures and secure timestamps of both the app and its embedded extension before distribution. Signing identifies the developer and lets macOS detect changes made to the bundle after it was signed; it does not mean Apple has inspected the software for malicious content.
- **Notarization:** The signed app and its signed DMG are submitted to Apple's notary service. Their accepted tickets are stapled to the distributed artifacts and checked with Gatekeeper/stapler tooling. Notarization gives macOS evidence that Apple scanned the submitted build and found no known malicious content, while stapling makes that evidence available even when the Mac is offline.

These layers matter together: the sandbox reduces the app's reach, signing protects identity and integrity, and notarization supports a trusted Gatekeeper launch experience. A local debug build is intended only for development and is not a substitute for the signed, notarized release produced by `make build`. Users should obtain releases from a trusted project channel; no security mechanism can make an untrusted download source safe.


