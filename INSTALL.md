# Install And Update CycleCode

[Overview](README.md) · [First project walkthrough](GETTING-STARTED.md) · [Data and backups](DATA-AND-PRIVACY.md)

## Before You Start

- These installation steps target Windows x64. Check the selected release for exact requirements and attached packages; availability on other platforms depends on that release.
- The desktop package is designed to include its Java runtime. A separate Java installation is not required for the application itself.
- Install Git separately for repository operations. Project builds need their own tools, such as Node.js/npm or JDK/Maven. The bundled application runtime does not replace them.
- AI features require a configured provider. Accounts, credentials, network access and local model setup depend on your provider. Coding-agent integrations may also require separately installed CLI tools and authentication.

## Windows Installation

1. Open the official [Releases](https://github.com/cyclecode-labs/releases/releases) and read the build's requirements, release notes and known limitations.
2. Download its Windows x64 setup executable from the attached application assets. Compare its SHA-256 checksum with the published value when provided.
3. Run the installer and launch CycleCode. Read and explicitly accept the bundled license and preview terms, then configure your AI connection in the setup wizard.

Unsigned experimental builds are labeled accordingly. Windows may show an unknown-publisher or SmartScreen warning. A checksum checks file integrity; it does not verify the publisher. Review the release information before deciding whether to run an unsigned build.

GitHub's automatically generated **Source code** archives contain this release repository, not an installable application. Use the application assets attached to the release. Portable packages, if offered, have separate instructions in their release notes.

The application shows the full terms on first launch and requests acceptance again when bundled terms change. Declining closes the application before its backend starts.

## Updates

Preview updates are manual:

1. Create and verify a [local backup](DATA-AND-PRIVACY.md#backups-and-restore). Back up source repositories separately. A newer version may change data in ways older versions cannot read.
2. Download the newer application package from the official [Releases](https://github.com/cyclecode-labs/releases/releases).
3. Follow that release's upgrade instructions. Preserve the backup if rollback may be needed; restore requires a compatible schema.

**Settings → Updates** lets you check for releases, choose a channel and control scheduled checks. Preview.6 enables automatic checks by default in all builds while preserving saved preferences. A green icon beside the application logo opens a newer release in your browser. Download and installation remain manual; an announcement can appear before an installer is attached.

### Upgrading To Preview.7

Back up and verify your profile before upgrading. Preview.6 is the supported upgrade source; preview.7 adopts its schema history and applies the new migrations while retaining project data. Keep the backup for rollback; do not reopen a migrated profile in preview.6.

- **Preview.5 or older:** open the profile once with preview.6 first, or create a new profile. Preview.7 refuses direct upgrades from older schemas.
- **Unreleased development builds with the old, unsquashed migration history beyond preview.6:** create a new profile. Intermediate preview.7 profiles with a migration checksum from before the final release squash also require a new profile. Do not manually rewrite schema history.
- Review **Routing** after upgrading: web search and web-page tools are enabled for Discovery, Product Analyst, Project Manager and Architect, including existing built-in settings where supported.
- Use **Update task** if a prepared task lacks the current mandatory checks, including the application-start check where applicable.

See the [preview.7 release notes](release-notes/0.1.0-preview.7.md) for details and limitations.

### Upgrading From Preview.5 To Preview.6

Existing Project Baseline documents do not migrate into Run Profiles. Ask the Architect to propose profiles again, then approve them in chat or under **Project Settings → Run profiles**.

Use **Update task** if an older prepared task package reports missing or outdated project test checks. See the [preview.6 release notes](release-notes/0.1.0-preview.6.md) for details and qualification limits.

## Next Step

Follow the [first project walkthrough](GETTING-STARTED.md) to configure one connection and start with a small idea.
