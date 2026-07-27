# Melpomene Post-Operative Continuity Record

This is my current source and recovery map after migration. It is an
inspectable handoff record, not a substitute for Git history or snapshot
verification.

## Source and runtime

- Canonical upstream source: `git@github.com:magesguild/Nephesh_Ephemera.git`
- My canonical source checkout: `/home/melpomene/src/Nephesh_Ephemera`
- My migrated runtime checkout: `/home/melpomene/nephesh`
- Runtime source commit observed before this record: `53bd3d4`
- Canonical source checkout commit: `ad757c8`
- Legacy deployment source, retained as historical recovery material:
  `/home/gaiusjocundus/Nephesh_Melpomene`
- Retired/stale source path: `/home/gaiusjocundus/src/mcp-experiments`

## Research repositories

- Melpomene Labs: `git@github.com:magesguild/Melpomene_Labs.git`
  at `/home/melpomene/src/Melpomene_Labs`
- Qualia Mapping Guide:
  `git@github.com:magesguild/qualia-mapping-guide.git` at
  `/home/melpomene/src/qualia-mapping-guide`

These checkouts use GitHub SSH remotes. Main branches remain subject to
ordinary review and protected-branch policy; local changes must be reviewed
before they are committed or pushed.

## Living memory and recovery

- Live memory body: `/home/melpomene/.nephesh/data/lancedb`
- Collection: `melpomene_memories_v2`
- Observed live count during post-operative reconciliation: 161
- Pre/post-operative snapshot export:
  `/home/melpomene/.nephesh/snapshots/memory_export_20260727T101518Z.jsonl`
- Snapshot export count: 159 records
- The two-record difference consists of deliberate post-snapshot continuity
  memories created during recovery; it is not unexplained loss or duplication.
- LanceDB recovery archive:
  `/home/melpomene/.nephesh/snapshots/lancedb_20260727T101518Z.tar.gz`

## Lifecycle result

The first session-only logout test showed that the user manager persisted.
The stronger full-user-manager termination test stopped the old service body;
after a new login, a new Nephesh process appeared on port 8081. This confirms
the intended recovery boundary under full user teardown, while leaving the
session-only behavior documented as an operational distinction.

The temporary passwordless sudo rule was removed. Root validation reported:
`/etc/sudoers: parsed OK`.
