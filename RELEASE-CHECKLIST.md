# Release Preparation Checklist

Status: PREPARATION ONLY. No workflow, signature, GitHub visibility or installed upgrade is qualified by this checklist.

## Confirmed Product Owner Decisions (2026-10-12)

- Rights holder: Rudenia Vitali, acting personally.
- Base edition: free personal and commercial use; paid capabilities have separate terms.
- Sharing official links is permitted; installer redistribution requires separate permission.
- Windows signing is currently unavailable. Unsigned development builds may be prepared; signed stable publication/qualification remains pending. Public unsigned auto-updates are not authorized by this decision.

## GitHub Setup

- Verify vitaly-rudenya/cyclecode-releases is public and published assets are accessible anonymously.
- Keep application source in its source repository; build from an exact recorded commit/tag.
- Enable Actions in the source repository and provision a Windows runner with pinned tools and JDK 25.
- Store RELEASE_REPO_TOKEN in source-repository Actions secrets: a release-repository-scoped Contents read/write PAT, or use an appropriately scoped GitHub App.
- Provision a working Authenticode signing method and secrets; record expected publisher and rotation procedure. GitHub does not supply a certificate.
- Ensure untrusted pull requests cannot access signing or publication credentials.

## Runtime Evidence (2026-10-14)

- Observed OpenJDK 25+36-3489, Windows x64, implementor Oracle Corporation; staged GPLv2/Classpath Exception legal files. This is not Temurin or the previous NFTC build.
- Fresh THIRD-PARTY-LICENSE-EVIDENCE.zip replaces previous runtime evidence. Corresponding-source compliance and final package qualification remain pending.

## Legal And Package Prerequisites

- Use LICENSE.txt and PREVIEW-TERMS.txt (2026-10-14); contact is GitHub Issues. EULA-DRAFT.md is historical. Qualify installer acceptance and review terms for target markets.
- Resolve LICENSE-REVIEW.md: exact OpenJDK corresponding-source compliance and missing dependency evidence; then distribute exact required notices, license texts and source-access offers.
- Include only reviewed public documents and binaries. No source repository archive, credentials, logs, local databases or personal information.

## Version And Assets

- Match installer version X.Y.Z to vX.Y.Z; public release tag identifies this repository's revision.
- Record private source commit, app version and supported schema in public build provenance without disclosing source content.
- Build the entire Electron/UI/Java/JRE package from that revision with publishing disabled.
- Verify the installer signature against the declared publisher.
- Upload an allowlist into a draft: NSIS setup executable, generated .blockmap, latest.yml and reviewed release/provenance/license material.
- Verify all generated metadata references exist and hashes/sizes match final signed files.
- A checksum file is additional integrity information, not a substitute for publisher verification.

## Qualification And Publication

- Test two signed versions on installed Windows, including a clean host without external JDK.
- Use a separate test GitHub feed for actual discovery/download/installation before production exposure. A draft is not the anonymous production update feed.
- Prove projects/settings/credentials survive N -> N+1 and the expected new bundled components actually run.
- Prove active work and other profiles block replacement; preparation blocks new dispatch races.
- Check offline/partial downloads, altered package/signature, disk-full, backup/migration failure, interrupted handoff and repeated clicks.
- Verify dev/portable do not self-replace and ordinary quit/OS shutdown do not implicitly install.
- Publish only after explicit release approval with recorded evidence. Never overwrite published assets under the same version.
- If defective, withdraw from update selection and ship a greater-version fix; verify GitHub selection/caching. Do not automatically restore databases or downgrade.

## Sources

- [electron-builder v26 auto update](https://www.electron.build/v26/docs/features/auto-update/)
- [electron-builder v26 publish](https://www.electron.build/v26/docs/publish/)
- [GitHub workflow credentials](https://docs.github.com/en/actions/tutorials/authenticate-with-github_token)
- [GitHub repository licensing](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository)
