# License Review And Runtime Evidence

- Updated: 2026-10-14.
- Status: base-edition/preview terms prepared; current runtime license evidence refreshed; full distribution clearance and installed-package qualification remain incomplete.
- Rights holder: Rudenia Vitali, acting personally. Free personal and commercial base-edition use; paid capabilities have separate terms. Official links may be shared; installer redistribution requires separate permission.
- Contact: https://github.com/vitaly-rudenya/cyclecode-releases/issues

## Current Java Runtime

The staged jlink runtime now contains GPLv2 with Classpath Exception in `legal/java.base/LICENSE`, replacing the earlier NFTC runtime evidence. The current build JDK metadata identifies OpenJDK `25+36-3489`, Windows x64, implementor Oracle Corporation, source revision `6c48f4ed707b`. This is an Oracle-produced OpenJDK build, not Oracle JDK under NFTC and not Eclipse Temurin. Implementor identity alone does not identify the license.

The fresh evidence archive includes staged runtime legal files, staged release metadata, original build-JDK release metadata and SHA-256 provenance for the build metadata/runtime executable/license. The old NFTC archive has been replaced; it is not mixed into this collection.

OpenJDK is still third-party software. Preserve all relevant license/exception/copyright texts and establish the GPL corresponding-source distribution mechanism for the exact shipped build and jlink output. Local `lib/src.zip` exists, but that alone is not evidence of complete corresponding source, build scripts or fulfilled recipient rights. A generic source URL or the mere presence of the GPL text is not full source compliance. Application proprietary terms do not restrict OpenJDK recipient rights.

## Collected Original Texts

[THIRD-PARTY-LICENSE-EVIDENCE.zip](THIRD-PARTY-LICENSE-EVIDENCE.zip) contains original license files and inventory regenerated from current local inputs: 427 component records, 15 open items. `inventory.json` binds the sidecar and UI lockfile hashes; `java-runtime/provenance.json` records runtime-specific evidence. These records are a conservative inventory, not the exact shipped component count or legal clearance.

The evidence collector preserves Electron/Chromium notices, all staged runtime legal files, available production npm legal texts and available original Java dependency notices. UI tree-shaking and shaded JAR metadata require comparison against the actual final binary and complete runtime dependency graph.

## Remaining Dependency Evidence

Original top-level license evidence remains missing for five UI packages: `cm6-theme-basic-light`, `format`, `mdast-util-highlight-mark`, `micromark-extension-highlight-mark`, `react-remove-scroll-bar`.

Original dependency legal text remains unresolved for seven Java records: `jsonschema-generator`, `jsonschema-module-jackson`, `jsonschema-module-swagger-2`, `gson`, `error_prone_annotations`, `standardwebhooks`, `annotations`.

Resolve version-matched original/parent notices and applicability; declared SPDX identifiers alone do not replace copyright notices or complete license texts. Verify bundled fonts/assets and installer plugins as well.

## Terms And Package Verification

[LICENSE.txt](LICENSE.txt) and [PREVIEW-TERMS.txt](PREVIEW-TERMS.txt) are the current authored terms; EULA-DRAFT.md is historical. These preserve statutory and third-party rights and make no claim of review by a lawyer for every market.

The source packaging configuration includes the terms in `resources/legal` and configures NSIS acceptance text. Actual NSIS acceptance, silent/portable consent, packaged runtime startup and clean-machine installation are not qualified by this document. Windows signing remains unavailable; preview updates remain manual.

## Before Binary Publication

1. Resolve exact OpenJDK corresponding-source obligations and dependency notice gaps.
2. Rebuild from a recorded revision and verify final package contents and license evidence match it.
3. Verify license page, runtime legal files, Electron notices and user-state preservation on installation.
4. Attach completed license material and required source delivery/offer to the preview release.

The prior NFTC-specific issue is superseded by the observed OpenJDK replacement. No remaining source-compliance or package-qualification item is silently marked complete.
