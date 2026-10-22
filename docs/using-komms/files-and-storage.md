# Files and storage

How files are encrypted and stored, how storage is counted, how long files are kept and what happens when a plan ends.

*Updated 21 October 2026*

You can share documents, images and video in any conversation. Files in private conversations are encrypted on your device before they're uploaded.

## Where files are stored

Files are encrypted and stored with independent storage providers, starting with Hippius, a decentralised storage network. Komms keeps a record of which workspace or person each file is charged to, so storage allowances can be enforced.

## File size

Each file can be up to **64 MiB** at launch. Larger files are planned for later.

## Whose storage a file uses

| What you share | Counts towards |
| --- | --- |
| Files in a workspace or server channel | That workspace's or server's storage |
| Files in direct messages and groups outside a workspace | Your personal storage |
| Your profile picture | Your personal storage |
| A workspace or server icon | That workspace's or server's storage |
| Backups of your own history | Your personal storage |

People receiving a file never pay for it. If the same file is shared twice in one workspace, it only counts once.

## Storage on each plan

Workspace and server storage depends on the plan: from 10 GB on the free plans to 1.5 TB on Scale. See [Plans and pricing](../getting-started/plans-and-pricing.md). Personal storage is 1 GB on the free plan.

New free workspaces start with 1 GB for their first 30 days, then move to the full 10 GB.

Members see the workspace's storage use, rounded, and their own contribution exactly. Admins see exact figures.

## How long files are kept

- **Free plans:** each file is kept for 12 months, on a rolling basis.
- **Paid plans:** files are kept for as long as the plan is active.

> [!NOTE]
> Komms doesn't sell permanent storage. Storage lasts while the plan, and the storage provider, are paid for.

## If a paid plan ends

1. If a yearly plan isn't renewed, storage becomes **read-only for 90 days** (14 days after a card payment is disputed). You can still read and export everything.
2. Renewing during that window restores everything as it was.
3. After the window, the **oldest files are removed first** until the workspace fits the free allowance. The workspace then carries on as a free one.

You can [export your history](export-your-history.md) at any time, including during the read-only window. An export can't bring back files that were already removed.

## Deleting files

Deleting a file releases its storage. Copies are removed from Komms and the provider is asked to delete them after a 48-hour hold. Komms can't promise a provider has physically erased every copy, and nobody can remove copies other people already downloaded.

## File transfers

Sending large files to people with an expiring link is **coming soon**. Until then, files you share count towards your storage.
