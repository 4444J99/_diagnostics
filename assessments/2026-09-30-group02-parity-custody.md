# Group 02 parity and custody checkpoint

Owners: [Domus E3](https://github.com/4444J99/domus-genoma/issues/397) and [PORTVS E2](https://github.com/4444J99/portvs/issues/14), with source custody supplied by the existing Limen E1/E5 recovery owners. This is an incomplete assessment checkpoint, not deletion eligibility, task completion or terminal session release.

Scope: exact Group 02 v3 allowlist, 11 repository views and six common Git stores; no bare-store candidates. IDs below follow allowlist order. Paths and file contents are redacted; SHA-256 path identities let the private allowlist resolve each retained copy.

Live GitHub immutable repository identities: Domus 1124448005 / R_kgDOQwW3BQ (private), PORTVS 1257137342 / R_kgDOSu5kvg, diagnostics 1248737661 / R_kgDOSm45fQ. Old organvm coordinates resolve to 4444J99 identities. Branch/tag advertisements succeeded for all six stores. Normal fetches refreshed remote tracking refs and tags; no local branch was reset, rebased or deleted. Configured fetch pruning affected tracking refs only. The nested lane needed an explicit all-head fetch because its configured fetch was restricted.

## Retained copies

| ID | Path SHA-256 | Status rows | Ignored entries | Retention reason |
|---|---|---:|---:|---|
| G02-01 | `b5fbf2cfbb9127aed43083b2c88f2a13526d9ce312f1858915403892adf4698b` | 3202 | 0 | Staged deletions; unreachable objects; LFS scan failed |
| G02-02 | `5b415bbb73ead81a59279e3e5d38bd81d602a89e83edb60bbdeead34282d4892` | 0 | 9 | Two branches outside fetched remote history; ignored payload; unreachable objects |
| G02-03 | `e11566eb4791c43226c98b1a5f19264dbd2c3ee44f05e358067035618fda40cc` | 0 | 0 | Unreachable objects require custody; receipt checkout retained |
| G02-04 | `a59aa1f24d434b41e412d001796dd0073dbfe990b0eb7d8f05c4cfbcd54ec66f` | 13 | 64089 | Active chezmoi source; dirty/untracked payload; stash; local-only history; shared dependents |
| G02-05 | `0a3ebbf659c4da52da577380e1f2b4d8505f09e8c11061acc87b031fafa2f9b2` | 0 | 10 | Ignored payload custody unproven |
| G02-06 | `c47e0bd0faa39839fd72820cca72f8e8b85576879bb9d0946c09a46b84c006d2` | 0 | 20 | Recent worktree retained by owning lifecycle |
| G02-07 | `42d48d3dc81c403fa1fa4a914b7aadcc0e20c3bf40a2a614bc2ff8ca60af3837` | 0 | 10526 | Recent worktree retained by owning lifecycle; ignored payload |
| G02-08 | `1c1b067cc0a3a8b0c13ae56c0b6c5406953a811a0081fdd68320aa00339561fc` | 1 | 31 | Dirty and untracked work owned by existing host-repair session |
| G02-09 | `6e4a9bb2418a7f8fe384f0b721c553bd5eca189a9bf0c9fc26e0851d424fbeb8` | 0 | 25 | Ignored payload custody unproven |
| G02-10 | `ea380d06f13818aef68ae7976e7a9efe4e8d105b4c5194d90f780589abee7f74` | 4 | 0 | Unborn lane container; untracked operational receipts and nested repository |
| G02-11 | `680da50c57f5a3b4fb08baa68440da9e16e91e7627f38152a1321d83d30b12a1` | 0 | 0 | All branch history reachable after full-head fetch; unreachable objects still need custody |

Counts are pre-fetch checkout observations, not unique payload sizes. Parent ignored/untracked listings may include allowed nested views; do not sum them. All 11 exact paths remain present; removed paths: none. Diagnostics now retains the published assessment branch as this session's artifact home.

## Parity and custody gaps

After full-head fetch, PORTVS remediate-1 has six commits outside fetched origin history and remediate-3 has two. Domus fix/cce-managed-refresh-20260925 has three, fix/domus-source-root-reconcile-20260925 has one, and fix/security-hardening-domus-genoma has three. These are reachability gaps, not proof that GitHub PR refs lack the objects. No blind push was performed; original branches and work were retained pending owning secret-scan and publication reconciliation. Other existing local branch tips are reachable from fetched remote history; this does not provide complete metadata or private-payload custody.

All six full Git fsck invocations exited 0. Pre-fetch unreachable-object rows by store in first-appearance order: 13763, 10, 58, 955, 0, 17. Domus has one stash. Independent private custody and restore checks were not proven for these objects, reflogs, stash, indexes or non-Git payload. LFS scans exited 0 on five stores; the quarantine scan exited 2 with a missing historical object. Its LFS acceptance remains unmeasured, despite fsck exiting 0.

Chezmoi source-path confirms the primary Domus copy remains an operational source dependency. Visible lsof CWD inspection exited 0 with no matching CWD, but this does not establish complete broker lease, protected-session or loaded-consumer clearance.

The installed reclaim-worktrees check exited 0 and retained all five assigned worktrees: ignored-payload-custody-unproven (two), recent activity (two), dirty (one). Although supplied repository-root, it also inventoried out-of-scope roots and returned five out-of-scope candidates. No apply was run. A scope-contained retirement manifest is required before any application; do not reuse the returned campaign plan.

## Measurement and next actions

Data-volume available space was 15729852 KiB before assessment and 15626296 KiB after fetch/assessment, a decrease of 103556 KiB. No space reclamation is credited; concurrent host writes prevent attributing this change solely to the assessment.

1. E1/E5: preserve exact Git metadata, unreachable objects, stash and private payload in independent private custody, then verify restoration for each retained identity. Resolve quarantine LFS failure through its existing quarantine owner.
2. E3: reconcile the five local-history gaps through normal secret-scanned publication; finish chezmoi consumer detachment and existing host-repair owner work without adopting protected sessions.
3. E2/Limen reclaimer: establish exact-scope process/lease clearance and a scope-contained journaled retirement plan; re-probe live remote identity, custody and payload immediately before applying it. Record absent paths and measured space only after actual retirement.

No implementation gates were claimed: this change adds only this redacted receipt. Validate with git diff --check and effective normal commit/push hooks. No deletion, force push, hook bypass, cloud mutation or installed-runtime mutation occurred.

## Execution follow-up

Four local-history gaps were secret-scanned with gitleaks (exit 0), published through normal Git push/LFS hooks, and read back as exact live custody refs:

| Repository | Remote ref suffix under refs/heads/custody/group02-20260930/ | Full OID |
|---|---|---|
| PORTVS | remediate-1 | 766f3c7bb846a19857c33d55eb9307358fdb5aaf |
| PORTVS | remediate-3 | 95512d1eae587fe50c252531526ac83e52a1ede7 |
| Domus | fix/cce-managed-refresh-20260925 | 37bf9cbdfc8533efc646f5a9b83275a487f9d634 |
| Domus | fix/domus-source-root-reconcile-20260925 | aba45318eb2951e04e1284b8fcc1cfa94c2fbf35 |

Domus security-hardening history and its stash passed gitleaks but are not published. The normal branch push exhausted its 60-second deadline without a remote ref. The stash push was stopped by this session after inspecting its required objects: 11024 objects, 332719812 blob bytes, including blob a0bd10933fbf0a859d03a64ebaf6f0524cd1168d at 121773448 bytes. This exceeds the standard 100 MiB GitHub blob limit. No history rewrite, force push or LFS migration was performed. Native stash bf6230941c76a7756798df801e0cfc405d1e202a, its index parent, and security-hardening tip 663b3cc97b0acc1ad1f59d62483c4182e0191611 remain preserved locally. GitHub commit API lookups for both tips returned 404. These require encrypted independent custody, not a blind repeat of the push.

Quarantine fetched missing objects caa2d52f4a52bcc21f72c2b8e4ae8250e364a9d2 and abf9ab66cfc0824af2bf35d84681b9926ad0d56c successfully. Re-scanning advanced to missing object 0b8498c87ce9d644e52bbc5939f6f37f3157fdef (LFS scan exit 2); complete historical LFS enumeration remains unproven. No original ref or checkout was changed.

Independent custody is externally unavailable: only the boot volume is mounted; registered Archive4T and T7Recovery custody targets have no mounted volume and their paired registry reports registered_not_live_verified. The existing HORREVM status --strict exits 77, PARKED on L-CLOUD-EGRESS-CONSENT. Its approved payload list does not admit arbitrary Group 02 repository archives, so this session neither activated the rail nor expanded its egress scope. Original private payload and Git metadata remain retained.

Four publication gaps are resolved. The remaining acceptance requires an existing-owner independent encrypted custody target and restore proof for oversize history, stash, unreachable metadata and payload, plus operational and protected-session release before retirement. No repository removal or complete parity/custody claim is made.
