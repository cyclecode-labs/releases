# CycleCode Releases

Official distribution repository for CycleCode, a local-first desktop workspace for product definition, role-based AI agents and controlled software delivery.

## Distribution Status

This repository is being prepared for releases. No production installer or functioning auto-update service is asserted by this README. See the [Releases page](https://github.com/vitaly-rudenya/cyclecode-releases/releases) for published versions when available.

The base edition is intended for free personal and commercial use. Rights holder: Rudenia Vitali, acting personally. Paid capabilities will have separate terms. Application source code is not distributed here. Final usage terms and third-party notices must accompany each production release.

## Planned Windows Installation

1. Download the Windows x64 NSIS setup executable from a published release.
2. For a signed production release, verify its publisher against the identity documented in that release. Windows signing is currently unavailable; only clearly labeled unsigned development preparation is planned until signing is provisioned.
3. Install and launch CycleCode. The installer will include its required Java runtime.

Never treat an unsigned development build as a verified production release. Portable builds, if offered, require manual replacement.

## Planned Updates

Installed Windows builds will check GitHub Releases and download a complete application package according to user preferences. Installation will require an explicit user action and safe runtime shutdown. Active tasks or another session using the installation will block replacement. The first updater-enabled version must be installed manually.

These capabilities are planned, not implemented by this repository. Users will not need a GitHub account or access token for public downloads.

## License And Terms

Rights holder: Rudenia Vitali, acting personally. The base edition permits free personal and commercial use. Paid capabilities have separate terms. Sharing official download links is permitted; republishing installers requires separate permission.

- [LICENSE.txt](LICENSE.txt): base-edition proprietary terms, version 1.0, 14 October 2026.
- [PREVIEW-TERMS.txt](PREVIEW-TERMS.txt): additional terms for unsigned experimental builds and manual updates.
- [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt): location/status of original dependency license evidence.
- [LICENSE-REVIEW.md](LICENSE-REVIEW.md): outstanding runtime/dependency checks. Distribution clearance is not complete.
- [GitHub Issues](https://github.com/vitaly-rudenya/cyclecode-releases/issues): license questions and redistribution permission requests. Do not post secrets or confidential materials.

Third-party components retain their original licenses. The staged runtime now uses OpenJDK 25+36-3489 under GPLv2 with Classpath Exception. Complete corresponding-source compliance and missing dependency notices require resolution before binary publication. The older EULA-DRAFT.md is historical and superseded by the terms above.

## Release Preparation

See [RELEASE-CHECKLIST.md](RELEASE-CHECKLIST.md) for GitHub setup, artifact requirements, legal prerequisites and installed-update validation. Maintainers should link users to official release downloads.
