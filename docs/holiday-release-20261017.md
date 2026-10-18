# Holiday release integration

REQ-HREL-001: WHEN building the holiday release THE SYSTEM SHALL retain current parent-network features and resolve the exact reviewed component pins below.
REQ-HREL-002: WHEN an explicitly approved fork is selected as the temporary release source THE SYSTEM SHALL use its merged default branch, retain upstream ancestry, and record that fork identity rather than claiming a parent merge.
REQ-HREL-003: IF any selected source is unmerged or a required build is incomplete THEN THE SYSTEM SHALL withhold production release approval.
REQ-HREL-004: WHEN preparing production rollback THE SYSTEM SHALL retain current artifacts, configuration and matched data/identity history without activating the release or resetting live claims.

The owner approved the merged Tags fork as the temporary release source on 17 October after the canonical merge returned HTTP403. This integration therefore changes the Tags submodule URL explicitly to FainNeito/EnthusiaTags. It does not impersonate a canonical Tags or Network merge. The release Network source is the owner's merged fork; upstream PR191 remains open for independent review. No security/build gate is waived by selecting a fork.

## Exact sources

| Component | Approved repository | Commit | Build |
|---|---|---|---|
| Tags | FainNeito/EnthusiaTags | 111d95af189c09d1f4c4b0d2dde34c3ccc52284e | Network gitlink; merged fork main, contains parent 28048ca |
| Renderer | BadgersMC/EnthusiaAdvancements | 01fac426152737c76cd4d2e570e07a33dde99798 | Network gitlink; canonical merged |
| Guilds | BadgersMC/LumaGuilds | 283d75f1e1016d415aa5afdfac840252f0391846 | Network gitlink; canonical v3.0.39 |
| Holidays | FainNeito/EnthusiaHolidays | d07390924de3a953a0685958325de6cf24e85d8d | Standalone canonical Gradle build; merged PR29 |
| UAA | FainNeito/UltimateAdvancementAPI | 94b59a461bcdd0452b98dbdf3536a678b77839ac | Standalone fork Maven build; merged PR2, contains current parent |

Unrelated Network pins and parent features are retained from canonical main 559bfabc2187ab796a3be889f032383a8041f819. The owner Network fork already contains that parent. The historical Tags/renderer and Guild-Staff bootstrap reconciliation remains in this branch. Guild Staff API is built from verified wsg138/EnthusiaStaff commit 8539bb8c77d7ecaf083546dda7ca8ccbfa8064e6; dirty or mismatched sources are rejected. No loose or stub API is committed.

Holidays and UAA are not Network submodules; retain their canonical standalone build paths and record their hashes in the release manifest. Do not claim the renderer's Maven compile dependency packages the server's UAA runtime. The selected UAA keeps version 2.8.2, so source commit and hash distinguish the fork build.

## SPEAR and evidence

Spec: the requirements and approved source boundary above. Prove: the earlier strict Tags consumer/provider version check and bounded bootstrap regression failed before pin reconciliation; the real UAA refresh regression observed [select, remove, definitions, select] during a routine tick. Engine: dependency and CI bootstrap changes only in Network; the UAA fix uses progress-only packets for unchanged wrapper snapshots. Arch: preserve domain/persistence, reward and platform boundaries. No runtime plugin behavior is implemented in Network. Refine: existing component suites, actual renderer-to-UAA compatibility, current-head CI/review and the exact merged-fork combined build. No local EARS/state helper exists in Network; this manual record is validated by the existing Tags EARS helper where available.

Verified component results: canonical Holidays clean build and all eleven Paper profiles pass, 274 tests. Clean UAA merged-fork default Maven build passes 46 tests, both distributions, Javadocs and all 24 adapters. Renderer production and test sources compile against that exact new UAA API (all old UAA classpath entries removed), with 44 tests passing. Tags previously passed 278 Java tests, 11 bootstrap checks, 12 Node checks and EARS; Guilds previously passed 1,769 cases with 16 environment skips. Current combined build must be verified at its merged fork head; a component result is not that combined proof.

The workflow recognizes same-repository owner-fork runs and cross-fork PRs as public builds. Canonical trusted builds still require the private Display read token and approved dependency URLs/hashes. Public builds skip private Display and never count as its acceptance. Keep the existing private Display gate unchanged; verify its actual pinned source in an authorized local/trusted build for a complete release.

The owner confirmed the remaining gameplay checks working, including fresh payouts/Netherite, inventory handling, first finisher, Watcher eyes/music/advancements/disc. This is owner acceptance, distinct from independent replay. The new selected-tab transport fix is installed on TEST for a separate 30-second inspection check.

## Install and rollback boundary

Production has no Holidays directory/JAR at the backup baseline. Initial installation includes explicit module switches with hunt and Watcher off before startup; enable only on the owner's schedule. Do not import TEST hunts, databases, identity keys, staging events or TEST switches. Seasonal guild icons remain excluded; resource-pack reload is not authorized.

A production live rollback archive is stored without changing running plugins; six small Tags SQLite snapshots are integrity-verified. Large DB/sidecar copying is limited by panel size limits and an expired node download certificate. The live archive is not an atomic DB snapshot and has no independently verified remote SHA. Refresh with consistent stopped data at separately authorized activation, keeping DB/WAL and the hunt identity key together. Do not restore stale reward history or pay claims twice. No production activation occurred.

## Native Enthusia tab presentation follow-up

REQ-HREL-005: WHEN packaging the native tab presentation fix THE SYSTEM SHALL pin merged FainNeito/EnthusiaTags commit 6bbb2534cef121cce01223da0e536ea338fd6566 and preserve every other reviewed plugin pin.

The owner authorized review, conditional merge and production file replacement without restart. Tags PR11 is reviewed and merged; its exact PR-head build and Codacy gates passed. The clean merged component build verifies 285 tests. The new scoped logo model uses the existing pack asset. Provider reward cards retain their node IDs and move beside their provider advancements; extra rewards wrap into bounded rows. No reward, criterion, claim storage or permission semantics change.

This follow-up supersedes only the Tags pin in the table above. All other gitlinks and trusted private Display gates/inputs are unchanged. Network has no local EARS/state helper; this is source-pin/documentation integration, so behavioral proof and engine implementation remain in Tags. The meaningful integration proof is exact-head combined CI plus unchanged-pin inspection; hosted review/merged-head evidence and artifact hashes are retained in the release operations receipt.

Production replacement is file-only; no restart, reload or pack rebuild is authorized. New in-game client acceptance remains distinct from source/build proof and the interactive layout simulation.
