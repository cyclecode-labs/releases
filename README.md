# CycleCode

**Turn a product idea into a reviewable software delivery workflow.**

CycleCode is a local-first desktop workspace for developers and small teams who want to define a product, coordinate specialized AI agents, and review implementation and validation in one place.

This is the official release and feedback repository. Application source code is maintained privately.

> **Preview: 0.1.0-preview.5.** Read the [Release Notes](release-notes/0.1.0-preview.5.md) for changes since preview.4, upgrade instructions, and known limitations. Download application packages from [Releases](https://github.com/cyclecode-labs/releases/releases) when available. This is experimental software; production release qualification is still in progress.

## Work In One Project Workspace

- **Define the product before coding.** Develop an idea into requirements, a clickable prototype, architecture, and an implementation plan.
- **Coordinate specialized AI agents.** Keep product analysis, design, implementation, and validation connected through shared project artifacts.
- **Keep delivery reviewable.** Use explicit approval gates, bounded code changes, and inspectable validation results.
- **Start from an existing repository.** Build an understanding of the codebase and a backlog before choosing scoped changes.

Preview.5 adds editable task plans with dependency graphs, GitHub and Jira Cloud task intake, chat attachments, Markdown/HTML export, and local backup and recovery. Work Items bring together implementation, diff review, validation, and the accepted Git result. Runs shows agent progress and failure diagnostics. See the [Release Notes](release-notes/0.1.0-preview.5.md) for feature boundaries.

The intended path is **idea → requirements → prototype → architecture → plan → implementation → validation → delivery**. Approval gates keep product decisions and code changes reviewable. Preview capabilities have individual limitations; the complete workflow is still being qualified.

## Before You Start

- The Windows installation path below targets **Windows x64**. Check the selected release for exact system requirements and available packages.
- The desktop package is designed to include its required Java runtime, so a separate Java installation is not required for the application itself.
- Install Git separately for repository operations. Project builds also need the tools required by that project, such as Node.js/npm or a JDK/Maven; the bundled application runtime does not replace them.
- Configure your chosen AI provider before using AI features. Provider accounts, credentials, network access, and any local model setup depend on that provider. Coding-agent integrations may also require separately installed tools and authentication.
- The base edition is free for personal and commercial use. Model/API, hosting, and other third-party charges are separate.

Local-first means project state and artifacts are stored on your machine. Using an external AI provider can send project context to that provider; review your configuration before working with confidential material.

## Windows Installation

1. Open [Releases](https://github.com/cyclecode-labs/releases/releases) and read the build's requirements and known limitations.
2. Download its Windows x64 setup executable from the official release assets. Compare its SHA-256 checksum with the published value when provided.
3. Run the installer and launch CycleCode. Read and explicitly accept the bundled license and preview terms before using the application, then configure your AI provider.

Unsigned experimental builds are labeled accordingly. Windows may show an unknown-publisher or SmartScreen warning. A checksum checks file integrity; it does not verify the publisher. Review the release information before deciding whether to run an unsigned build.

Portable packages, if offered, have separate instructions in their release notes. Packaged applications also show the full terms on first launch and request acceptance again when the bundled terms change. Declining closes the application before its backend starts.

GitHub's automatically generated **Source code** archives contain this release repository, not an installable application. Use the application assets attached to the release.

## First Launch

After accepting the terms, use the setup wizard to configure provider connections, assign agents to roles, and review readiness. Provider accounts and coding-agent CLI authentication are configured for the services you choose. You can revisit configuration in Settings.

Create a project from an idea or start repository onboarding. Work through the product artifacts and approval gates before preparing implementation tasks. For an existing repository, review the imported understanding and proposed work before authorizing changes.

Connect GitHub.com or Jira Cloud in **Settings → Integrations** to preview assigned tasks and adopt selected tasks into a project. This preview reads from those trackers; it does not update remote issues.

## Updates

Preview updates are manual: download the newer package from [Releases](https://github.com/cyclecode-labs/releases/releases) and follow its upgrade instructions. Back up your profile and projects first; a newer version may change data in ways older versions cannot read.

Preview.5 adds update discovery: **Settings → Updates** lets you check for releases, choose a channel, and control scheduled checks. A green icon beside the application logo opens a newer release in your browser. Download and installation remain manual; an announcement can appear before an installer is attached.

## Local Data And Backups

With the default Windows configuration, saved project data is in `%LOCALAPPDATA%\CycleCode\profile`, and desktop settings and protected credential storage are in `%APPDATA%\CycleCode`. Custom profile locations can differ.

Use **Settings → Storage And Backup** to inspect profile disk usage, create a local backup, verify it, or restore it with confirmation and a restart. Backups contain the database and referenced managed content, including saved documents and chat attachments. They are unencrypted local folders and can contain sensitive project text.

Back up source repositories separately. CycleCode backups exclude repository files, worktrees, credentials, and external coding-agent history. Restore currently targets the same configured profile location and compatible schema; it is not a profile migration to another machine. Markdown/HTML exports are readable snapshots and cannot restore a profile.

## Feedback And Support

Use [GitHub Issues](https://github.com/cyclecode-labs/releases/issues) to report bugs, suggest improvements, ask license questions, or request redistribution permission. For bugs, include the application version, operating system, steps to reproduce, and expected and actual behavior.

Do not post API keys, tokens, credentials, confidential project content, or unredacted logs in public issues.

## License And Third-Party Software

Copyright © 2026 Rudenia Vitali. All rights reserved in proprietary components.

- [LICENSE.txt](LICENSE.txt): proprietary base-edition terms, including free personal and commercial use. Paid capabilities have separate terms.
- [PREVIEW-TERMS.txt](PREVIEW-TERMS.txt): additional terms for experimental builds and manual updates.
- [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt) and [THIRD-PARTY-LICENSE-EVIDENCE.zip](THIRD-PARTY-LICENSE-EVIDENCE.zip): third-party component notices, collected license texts, and OpenJDK GPLv2 with Classpath Exception source-access provenance. Third-party components retain their own licenses and rights.

Sharing official download links is welcome. Republishing installers requires separate permission, subject to applicable law and third-party licenses.
