# Export your history

The planned full private-history export and its verification limits.

*Updated 30 October 2026*

> [!NOTE]
> Full private-history export is planned, not available. Current public-channel JSON export is not a complete private-history archive. The rest of this guide describes the intended export design. See [Network status](../network/network-status.md) for availability.

Once released, full private-history export is intended to be available on every plan, including during a paid plan's read-only period. An export contains only what your device can retrieve; it cannot recreate missing messages, expired files or unavailable keys.

## What's in an export

- Messages and files available to your device
- Identity and anchor records needed to check those messages
- Each item's recorded verification result and its observation context

## Offline and fresh checks

Offline checks can test the included signatures and record consistency. They cannot establish today's live identity state or detect every omission from an archive.

A fresh network check also needs the required public records, a pinned covenant template and node access while the author's identity remains open. Verification uses your own node or two independently operated nodes. One node gives a weaker observation.

| Result | Meaning |
| --- | --- |
| Verified | The required checks succeeded using your own node or two independent operators |
| Single node | A check based on one operator only |
| Cannot check | Required network state, records or other evidence are unavailable |
| Not found | No matching record was found in the queried source |
| Failed | The supplied records fail the required consistency or authorisation checks |

Closing an identity prevents a fresh successful live-identity check. A result recorded before closure remains an earlier observation, not proof of current state. Full private-history export is not available, so do not close an identity in reliance on that planned feature. See [Close your account](close-your-account.md).

A successful check establishes the signature and place in the author's anchored history. It does not establish exact send time, physical device or rightful key ownership.

## Backups and keys

History-backup keys derive from the device's master seed. A recovery kit contains a separate recovery secret. Recovery of identity control onto a new master seed is planned, not shipped; the kit cannot decrypt old history by itself. Restoring an old backup requires its archive key and retained data. See [Your recovery kit](../security-and-privacy/recovery-kit.md).

Workspace and server backup policies govern which conversation data clients back up. When full export is released, keep a separate export for important records and protect it: a readable export can disclose conversation content to whoever receives it.

## Limits

An export cannot recover files already deleted after a plan lapse, messages no device of yours received, or records no longer available from storage. It also cannot erase copies held by other people.
