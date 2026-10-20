# CycleCode

**Turn a product idea into a reviewable software delivery workflow.**

CycleCode is a local-first desktop workspace for developers and small teams who want to define a product, coordinate specialized AI agents, and review implementation and validation in one place.

This is the official release and feedback repository. Application source code is maintained privately.

> **Status: Pre-release preparation.** Check [Releases](https://github.com/vitaly-rudenya/cyclecode-releases/releases) for available builds and their supported features, requirements, and known limitations. Production release qualification is still in progress.

## What CycleCode Is Designed To Do

- **Define the product before coding.** Develop an idea into requirements, a clickable prototype, architecture, and an implementation plan.
- **Coordinate specialized AI agents.** Keep product analysis, design, implementation, and validation connected through shared project artifacts.
- **Keep delivery reviewable.** Use explicit approval gates, bounded code changes, and inspectable validation results.
- **Start from an existing repository.** Build an understanding of the codebase and a backlog before choosing scoped changes.

The intended path is **idea → requirements → prototype → architecture → plan → implementation → validation → delivery**. The capabilities above describe the product direction; individual preview releases may support only part of this workflow.

## Before You Start

- The Windows installation path below targets **Windows x64**. Check the selected release for exact system requirements and available packages.
- The desktop package is designed to include its required Java runtime, so a separate Java installation is not required for the application itself.
- Configure your chosen AI provider before using AI features. Provider accounts, credentials, network access, and any local model setup depend on that provider. Coding-agent integrations may also require separately installed tools and authentication.
- The base edition is free for personal and commercial use. Model/API, hosting, and other third-party charges are separate.

Local-first means project state and artifacts are stored on your machine. Using an external AI provider can send project context to that provider; review your configuration before working with confidential material.

## Windows Installation

When a Windows preview is available:

1. Open [Releases](https://github.com/vitaly-rudenya/cyclecode-releases/releases) and read the build's requirements and known limitations.
2. Download its Windows x64 setup executable from the official release assets. Compare its SHA-256 checksum with the published value when provided.
3. Run the installer and launch CycleCode, then configure your AI provider.

Unsigned experimental builds are labeled accordingly. Windows may show an unknown-publisher or SmartScreen warning. A checksum checks file integrity; it does not verify the publisher. Review the release information before deciding whether to run an unsigned build.

Portable packages, if offered, have separate instructions in their release notes.

## Updates

Preview updates are manual: download the newer package from [Releases](https://github.com/vitaly-rudenya/cyclecode-releases/releases) and follow its upgrade instructions. Back up your profile and projects first; a newer version may change data in ways older versions cannot read.

In-app updates are planned. Until a release explicitly documents their availability, use manual updates.

## Feedback And Support

Use [GitHub Issues](https://github.com/vitaly-rudenya/cyclecode-releases/issues) to report bugs, suggest improvements, ask license questions, or request redistribution permission. For bugs, include the application version, operating system, steps to reproduce, and expected and actual behavior.

Do not post API keys, tokens, credentials, confidential project content, or unredacted logs in public issues.

## License And Third-Party Software

Copyright © 2026 Rudenia Vitali. All rights reserved in proprietary components.

- [LICENSE.txt](LICENSE.txt): proprietary base-edition terms, including free personal and commercial use. Paid capabilities have separate terms.
- [PREVIEW-TERMS.txt](PREVIEW-TERMS.txt): additional terms for experimental builds and manual updates.
- [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt): collected dependency license evidence and its current coverage status. Third-party components retain their own licenses and rights.

Sharing official download links is welcome. Republishing installers requires separate permission, subject to applicable law and third-party licenses.

## For Maintainers

Publication requirements are tracked in [RELEASE-CHECKLIST.md](RELEASE-CHECKLIST.md). [LICENSE-REVIEW.md](LICENSE-REVIEW.md) records unresolved runtime source-compliance and dependency-notice checks that must be completed before binary publication.
