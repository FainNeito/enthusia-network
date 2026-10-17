# Holiday release candidate reconciliation

## Scope and requirements

REQ-HREL-001: WHEN building the holiday candidate THE SYSTEM SHALL retain current canonical network features and resolve the exact Tags, advancement renderer and LumaGuilds commits listed below.

REQ-HREL-002: IF a component has not merged into its canonical default branch THEN THE SYSTEM SHALL label this combined build as a testing candidate and require canonical merge/pin reconciliation before production delivery.

This branch starts from canonical network main 559bfab and changes three existing submodule pins plus a fork-only CI classification correction and this evidence. It does not reset the network to an older owner-fork branch, redesign menus, install plugins, reload the resource pack or enable any holiday activity.

## Component pins

| Component | Repository | Selected source | Status |
|---|---|---|---|
| EnthusiaTags | wsg138/EnthusiaTags | 111d95af189c09d1f4c4b0d2dde34c3ccc52284e | Owner fork main; canonical PR29 pending maintainer merge |
| Advancement renderer | BadgersMC/EnthusiaAdvancements | 01fac426152737c76cd4d2e570e07a33dde99798 | Canonical merged PR23 |
| LumaGuilds | BadgersMC/LumaGuilds | 283d75f1e1016d415aa5afdfac840252f0391846 | Canonical main; release v3.0.39 |
| EnthusiaHolidays | FainNeito/EnthusiaHolidays | 9926be709e9778fc2be3f45d40fc9aa74ce8d336 | Canonical merged PR23; built separately |

Holidays is not currently a network submodule. Keep its existing standalone canonical Gradle build; this change does not add a private checkout to the public submodule loop or weaken the existing private Display verification gate.

## Fork preservation audit

- Tags already contains canonical parent main 28048ca. Retain its production menu restoration, reward hierarchy, provider categories, holiday tags and ownership/history migrations. The new fork PR10 updates only the renderer pin/version, bounded bootstrap validation and evidence.
- Advancements' old fork pilot tree matches the earlier canonical squash 5a96728. Synchronization retains all newer parent progression events, companion compatibility, verified eKOTH and AxKoth retirement; merged owner-fork PR10 has the same source tree as current canonical 01fac426.
- LumaGuilds' holiday themes, conditional revoke fixes, insert-column correction and Chapter 2 rewards already landed upstream. Current parent also contains the earned Pumpkin King guild emoji. Synchronize the owner fork to the exact current parent tree, retaining old ancestry only in that fork. Do not restore the intentionally retired AxKoth hook, old private pack bytes or send old history back to the sanitized parent.
- The old network fork main is an ancestor of current canonical main. Unrelated pins and build behavior remain unchanged.

## SPEAR and verification

Spec: requirements and component selection above. Prove: the existing strict scripts/build-tags.sh consumer/provider version check rejects the old Tags pilot pin after the renderer update. Tags' bootstrap regression failed before the bounded version allowlist/pin fix. Engine: reconcile only selected dependency pins. Arch: no domain, persistence, permission, reward-dispatch or GUI behavior changes in the network repository. Refine: run existing component suites, actual pinned renderer-to-Tags verification, exact-head hosted checks and git diff --check. No project-local EARS/state helper exists here; use the existing Tags EARS tool for this scoped record and retain manual evidence.

Local results: canonical Holidays clean build and all 11 supported Paper compile profiles pass, 273 tests; canonical advancement pilot clean install passes 44 tests; Tags clean verify against that actual provider passes 278 tests; LumaGuilds current-parent clean test/shadowJar passes 1,769 test cases, zero failures/errors and 16 environment skips. Tags additionally passes 11 Python bootstrap regressions, 12 Node state/tooling tests and EARS. These are component/source checks, not a claim that the full network CI, private Display gate, MariaDB profiles or Minecraft clients have passed.

The owner's fork PR reproduced a CI classification failure: a same-repository PR in a fork required the canonical private Display token. Recognize the event repository's fork flag as well as cross-repository PRs, matching the existing public-fork verification policy. Truth table: owner-fork PR/push skips private Display; cross-fork PR into canonical also skips it; canonical push and canonical same-repository PR still require its private token and approved API variables. No runtime behavior or canonical trusted gate changes. A successful public build must never be reported as private Display acceptance.

## Release gates

The account preparing this candidate cannot merge canonical Tags PR29 or the canonical network PR. After maintainers merge, replace the Tags pin with its exact canonical merge commit and reverify the combined head before producing production artifacts. Keep both the hunt and Watcher disabled for initial installation. Watcher player acceptance and its missing dispatch acknowledgement/replay remain separate release blockers. Seasonal guild icons remain excluded and no pack reload is authorized.
