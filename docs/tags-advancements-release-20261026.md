# Paired Tags and advancement pilot release

## Spec and pins

REQ-003 pins reviewed Tags380497fd7ae15fdc6eb19365eae308967348bff2 and canonical Advancements01fac426152737c76cd4d2e570e07a33dde99798. Canonical Tags PR32 must merge before network release acceptance; a fork-only merge is insufficient. All other gitlinks and build scripts remain unchanged.

## SPEAR infrastructure evidence

Current canonical network main559bfabc2187ab796a3be889f032383a8041f819 was fetched and an isolated worktree created. Existing owner branches/worktrees remain untouched. Spec and architecture preserve source ownership and the actual network pilot API dependency; prove/engine do not apply to immutable build pins. Use the pinned Tags EARS/state helpers for the root infrastructure cycle. No gameplay test failures are invented for this pin change.

Tags fork PR17 has305 passing Java tests,12 Node tooling tests,11 Python bootstrap tests, architecture/EARS and shaded SQLite checks; exact-head hosted verify/artifact/strict Codacy passed. Canonical PR32 hosted results and the paired build are separate release gates. Advancements canonical main verify passed. CodeRabbit skipped the fork review, not an independent approval.

## Runtime profile and acceptance

Deploy only the Maven pilot renderer (`pilot/target/EnthusiaAdvancements-pilot-*.jar`) with Tags, never the alternative root Gradle renderer alongside it. Both profiles share the same plugin name. Tags requires pilot version1.0.0-pilot.6-watcher-brackets-test.6. The existing network helper installs that exact pinned pilot before Tags verification.

Prior SMP Test evidence verified exact compile/runtime ProjectionService and Node class bytes, startup, historical Frequent Shipper eligibility and reconnect persistence. It did not claim a reward or prove payout/duplicate-claim behavior; Diary/Discord icon and resource-pack acceptance remain incomplete. This release does not bundle pack/config changes.

User authorized production file staging and removal of superseded JARs after backup, explicitly without restart/reload. Production listing already names Advancements01fac426; filename alone is not hash/source proof. Check actual bytes and preserve unrelated plugins/config/player data. Verify clean merged source, combined build, artifact versions/hashes and unique rollback backups before writes. No runtime activation is claimed until a separately authorized restart loads the staged files.
