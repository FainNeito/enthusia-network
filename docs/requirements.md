# Monorepo integration requirements

### REQ-003 — Paired Tags and pilot renderer release

WHEN the paired Tags and advancement release is built THE SYSTEM SHALL verify the reviewed canonical merged Tags source against the pilot API from the pinned canonical EnthusiaAdvancements source while preserving every unrelated submodule pin.

Acceptance: Tags release head `380497fd7ae15fdc6eb19365eae308967348bff2` must be contained in merged canonical Tags main; renderer source is `01fac426152737c76cd4d2e570e07a33dde99798`. Run `scripts/build-tags.sh`, retain the pilot and root renderer profile distinction, and require exact-head hosted checks before merge. Production staging does not authorize restart or reload.

### REQ-001 — EnthusiaSignature build pin

WHEN the network build runs THE SYSTEM SHALL verify and package the reviewed EnthusiaSignature submodule with its tests enabled, retain all existing plugin pins, and report its shaded artifact.

Acceptance: Unix and Windows helpers and GitHub Build invoke `mvn -B -ntp clean verify`; the submodule points to merged ItemSignature commit `2e60f42d29d67dc610d16d6564b2251e58731a13`; upstream watch tracks its canonical repository.

### REQ-002 — Halloween asset verification

WHEN the network build verifies EnthusiaSignature THE SYSTEM SHALL run its Halloween importer regression checks using the pinned Python dependencies.

Acceptance: Unix and Windows helpers and CI run the nine importer checks from the pinned source. Licensed images remain outside Git, all other plugin pins remain unchanged, and live asset placement does not replace a plugin JAR or authorize activation.
