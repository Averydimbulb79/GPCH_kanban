# Repository working instructions

## Mandatory backup before changes

The owner requires a recoverable backup before every subsequent change batch, including UI, functionality, data migrations, and documentation changes.

1. Before editing, inspect the target branch and record its exact commit SHA.
2. Create a new uniquely named remote backup branch, such as backup/YYYY-MM-DD-HHMMSS-description, at that SHA. Verify the remote branch resolves to the recorded SHA before editing. Never overwrite, move, or delete an earlier backup.
3. If the live/default branch differs from the working branch and will be changed, back it up separately before changing it. Preserve any uncommitted work separately before editing.
4. Record the backup name, original branch, commit SHA, and purpose in the README/change notes for the update. Report the restore point to the owner.
5. Make each change batch in a separate commit. Restore application code using a revert commit or a reviewed restoration commit; do not force-push shared history. Retain these backup instructions when restoring older application code.
6. Code backups do not include browser localStorage records. Before any data migration or destructive data change, obtain a current app JSON export from the actual browser holding those records; do not claim Git backs them up.

## Initial restore points created 15 October 2026

| Backup branch | Original branch | Commit | Purpose |
| --- | --- | --- | --- |
| backup/2026-10-15-live | main | 5872c26616374b783654d37febbe67824cc92233 | Existing live application before v7.1 |
| backup/2026-10-15-v7-1-preview | improve/operations-ui-v7-1 | 1157e84a707bafb4ae56c9f29fcad203cba32d02 | Pending v7.1 interface including hotel logo |

## Incremental release workflow

The owner authorises direct live deployment of future updates after backups and appropriate checks; no extra merge confirmation is required. Update the version number and README for every incremental update, documenting changes, validation, known limitations and backup restore point. Verify deployment status and report accurately whether the release is live or pending.
