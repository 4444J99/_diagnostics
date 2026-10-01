# Group 02 remote preservation and retention receipt

Owners: Domus #397, PORTVS #14 and Limen #2740. This supersedes the custody gaps in the September 30 checkpoint while preserving that checkpoint's history.

The private Domus repository (immutable ID 1124448005) holds encrypted ARCA envelopes in release `custody-group02-20261001` (ID 401287970). Every canonical asset below was downloaded from GitHub, decrypted through the existing ARCA Keychain authority, and restored into session-owned scratch. Ciphertext and snapshot hashes matched; all captured regular-file bytes, modes and symlink targets matched the encrypted manifests. All six restored standalone Git stores passed `git fsck --full` with lazy network fetch disabled. Linked worktrees share the archived main Domus store; their absolute .git pointers and common-store registry remain in the encrypted manifests for reconstruction.

The archive covers committed source, refs/tags, stash and index state, reflogs, locally present unreachable objects, dirty/untracked files and selected ignored payload. Four ordinary history gaps were previously secret-scanned and published under additive refs. The remaining oversize Git history, stash and private configuration now have encrypted remote representations and proven restores without rewriting history.

Primary Domus excludes its 1.68 GB UV-managed cache from the canonical remote source archive. That cache remains untouched locally under the UV/package owner; the main checkout remains operational and cannot be retired on this receipt. All foreign nested Git roots are also excluded by exact scope, and allowed linked/nested views are captured separately. No filesystem-wide, package-cache, off-machine key-escrow or campaign completion claim is made.

| ID | Remote asset | Ciphertext SHA-256 | Restored entries |
|---|---|---|---|
| G02-01 | G02-01-hydrated.tar.enc | `56aa377f20cf837af16aa01c0f8282e4b80e73fcf88a166da065246df85994ab` | 158 |
| G02-02 | G02-02.tar.enc | `35286cbf0889360937dd1acb401a423949ce0f29240bf770d5187777010d714e` | 630 |
| G02-03 | G02-03.tar.enc | `a01df8e8fe46c621e89f43aaa3d7579e486b6e66aae8408f47ac11b4bb08adea` | 426 |
| G02-04 | G02-04-source.tar.enc | `2920e9c58f17d1d61615ba4b0d404dd3742d99100f3cf26030996bc610e63a26` | 5313 |
| G02-05 | G02-05.tar.enc | `f545663758bade50267768e071ac73847114796ee06b4a3a041d2796713c6afc` | 3637 |
| G02-06 | G02-06.tar.enc | `df3d10d5116ba37a826529773cfcc17fa2966e6597130ca409817aeb3abfa35f` | 3679 |
| G02-07 | G02-07.tar.enc | `4ae0f7c5066cf3ec56826fcdd4d0c6b978b4f422235cf298685d66056e59ee0d` | 15281 |
| G02-08 | G02-08.tar.enc | `0772b85d9c28db7e9a94f45d064c7e4a096f584ca6c8597a171f9440bf6dda6d` | 3841 |
| G02-09 | G02-09.tar.enc | `bd41dec0d958953c3f5604a93ae9b48b3d9f41deea7e728da43ef1e03ffa7440` | 3674 |
| G02-10 | G02-10.tar.enc | `e945652cda86c928215ff7d79ef8f026e80657b81ce00993f6419d4636ab09d5` | 239 |
| G02-11 | G02-11.tar.enc | `2114c9b78390719a88ed2d711c9274adc6d1e7bffde9fbd105bce8dc04fd105d` | 3767 |

## Quarantine repair

The quarantine was a blob-filtered partial clone. A bounded unfiltered refetch with no negotiation hydrated its history: `rev-list --objects --all --reflog --missing=print` reported zero missing objects and `git lfs ls-files --all --long` exited 0. The final G02-01-hydrated envelope preserves that repaired state. All six stores' LFS enumerations now exit 0 and contain zero LFS pointers.

## Exact retention dispositions

IDs follow the private Group 02 v3 allowlist, and JSON path hashes bind each exact original path. All 11 original paths remain present; no original source was relocated or deleted.

- G02-01: staged dirty quarantine state; preserved and retained with its existing quarantine/recovery owner.
- G02-02: PORTVS core/residency owner; source handoffs and encrypted metadata preserved, operational retention unchanged.
- G02-03: the clone classifier sees a pushed mirror, but this session retains its receipt checkout as the current artifact home pending its PR and session-release lifecycle.
- G02-04: active chezmoi source and common-store owner, with surviving linked worktrees and locally retained UV dependencies; Domus #397 owns detachment.
- G02-05 and G02-09: snapshots are restore-verified, but the installed reclaimer does not consume this custody format for ignored payload. Limen #2740 owns adoption into its recognized custody predicate; no bypass or force removal was performed.
- G02-06 and G02-07: the existing 24-hour lifecycle activity gate retains them; existing workstream owners remain responsible.
- G02-08: dirty host-repair work stays with its existing owner; this session did not adopt or commit it.
- G02-10: operational lane container with dirty/untracked receipts and excluded foreign nested repository; retained under its native lane owner.
- G02-11: the clone lifecycle reports unpushed objects; exact encrypted Git metadata has been preserved, but the native retirement predicate has not accepted that representation.

The contained worktree check scanned exactly five assigned worktrees, exited 0 and returned no candidates. Unlike the earlier default estate scan, it disabled only out-of-scope scan surfaces and retained the original 24-hour activity threshold. No safety, custody or acceptance predicate was weakened. The six standalone views were assessed with the installed read-only clone classifier; only the current artifact-home mirror passed its basic mirror classifier, and no apply was run.

## Reconstruction

Use authenticated `gh release download custody-group02-20261001 --repo 4444J99/domus-genoma --pattern ASSET --dir PRIVATE_DEST` for the canonical asset in the table. Check its SHA-256 against the tracked JSON, then use the installed `scripts/arca.sh unseal ASSET PRIVATE_RESTORE` with the existing authorized ARCA key. Each envelope contains an encrypted `manifest.json` and `snapshot.tar.gz`. The manifest supplies the exact original path, exclusions, modes, symlink targets and file hashes. Restore the common Domus store before its linked views; preserve the archived .git registry or repair pointers through native Git worktree repair at the restored paths. Do not overlay active originals. Key escrow remains with the existing key authority; this receipt proves an actual authorized restore, not independent key recovery after loss of that authority.

Remaining work is owned, not declared complete: the control-source detachment, protected-session release and recognized retirement-proof adoption stay with their existing owners. This Group 02 pass establishes source/metadata preservation and exact retention evidence, not permission to remove active, dirty, core or package-managed copies.

## Publication, cleanup and measurement

The custody release is published (not a draft), with eleven canonical verified envelopes, the earlier quarantine checkpoint and the redacted JSON receipt. Release JSON readback matched the git-tracked receipt byte for byte. All originals remain at their exact allowlisted paths. Three session-generated temporary capture/download/restore directories were removed after remote verification; no original repository or package cache was removed.

Data-volume available space immediately before temporary cleanup: 38461828 KiB; immediately after: 42478684 KiB, a measured increase of 4016856 KiB. This credits only this session's temporary cleanup, not estate/source retirement. Host-wide changes between the earlier census and these measurements are not attributed to this workstream. Original-repository reclamation credited: zero.

One exact-head merge submission for diagnostics PR #20 at cf7a20983d853533feb128fd15be01e9d58a5a7e exited 2 with `DEFERRED — LIFECYCLE-UNKNOWN`. No synchronous CI wait, repeated submission or merge claim followed. The repository lifecycle owner must resolve that existing rail; the PR remains the published durable home. This documentation-only measurement update is published to the same PR without retrying that unchanged lifecycle defect.
