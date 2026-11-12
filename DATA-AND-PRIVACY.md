# Local Data, Providers And Backups

[Overview](README.md) · [Installation and updates](INSTALL.md)

## Local Storage And External Providers

Local-first means project state and artifacts are stored on your machine. Using an external AI provider can send project context to that provider; review your configuration before working with confidential material. Provider accounts, credentials, network access and any local model setup depend on the provider you choose. Local CLI execution alone does not mean model inference stays on your device.

With the default Windows configuration:

| Location | Contents |
| --- | --- |
| `%LOCALAPPDATA%\CycleCode\profile` | Saved project data |
| `%APPDATA%\CycleCode` | Desktop settings and protected credential storage |

Custom profile locations can differ.

## Backups And Restore

Use **Settings → Storage And Backup** to inspect profile disk usage, create a local backup, verify it, or restore it with confirmation and a restart.

Backups contain the database and referenced managed content, including saved documents and chat attachments. They are unencrypted local folders and can contain sensitive project text. Store them accordingly.

Back up source repositories separately. CycleCode backups exclude repository files, worktrees, credentials and external coding-agent history.

Restore currently targets the same configured profile location and compatible schema. It is not a profile migration to another machine. Markdown/HTML exports are readable snapshots and cannot restore a profile.

Before an update, create and verify a backup and preserve it for rollback. Follow the selected release's [upgrade instructions](INSTALL.md#updates); older application versions may not read newer data.

## Public Feedback

Do not post API keys, tokens, credentials, confidential project content or unredacted logs in [public issues](https://github.com/cyclecode-labs/releases/issues). Review screenshots and exported content before sharing them.
