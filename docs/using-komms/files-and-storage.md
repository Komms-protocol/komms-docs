# Files and storage

How files are encrypted and stored, how storage is counted, how long files are kept and what happens when a plan ends.

*Updated 30 October 2026*

> [!NOTE]
> This guide describes the planned public beta. See [Network status](../network/network-status.md) for availability and qualification.

You can share documents, images and video in any conversation. Files in private conversations are encrypted on your device before they're uploaded.

## Where files are stored

Private-conversation files are encrypted before storage. The launch design uses a Komms-managed Hippius provider account with a same-host mirror; independent operator storage is a separate qualification step. The planned storage ledger would record which workspace or person each file is charged to. Live allowance enforcement remains unverified.

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

These are planned retention rules. Live retention enforcement and sweeps remain unverified.

- **Free plans:** each file is kept for 12 months, on a rolling basis.
- **Paid plans:** files are kept for as long as the plan is active.

> [!NOTE]
> Komms doesn't sell permanent storage. Storage lasts while the plan, and the storage provider, are paid for.

## If a paid plan ends

1. Under the planned lapse policy, if any paid plan lapses, whether billed yearly or monthly, storage becomes **read-only for 90 days**. A card payment dispute has a separate **14-day read-only period**. The design preserves read access to retained data during that period. Full private-history export is planned, not available.
2. Under that policy, renewal during the window would restore active access to retained files.
3. The planned sweep would then remove the **oldest files first** until the workspace fits the free allowance and continues as a free one. Live lapse handling and sweeps remain unverified.

Full private-history [export](export-your-history.md) is planned, not available. Once released, it is intended to work during the read-only window. An export cannot bring back files that were already removed.

## Deleting files

Under the planned deletion policy, deleting a file would release its storage claim. Serving would stop according to the applicable deletion rule, and the provider would be asked to delete eligible copies after a 48-hour hold. Another live claim could keep the same object stored. Live deletion and sweeps remain unverified; a testnet deletion does not establish storage removal or cessation of anonymous content-ID retrieval. Komms can't promise a provider has physically erased every copy, and nobody can remove copies other people already downloaded.

## File transfers

Sending large files to people with an expiring link is **coming soon**. Until then, files you share count towards your storage.
