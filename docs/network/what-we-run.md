# What Komms runs

The launch design's team-controlled services, their failure effects and the evidence needed to reduce that dependence.

*Updated 22 October 2026*

These are dependencies in the launch design, not a claim that all launch services are deployed. [Network status](network-status.md) is the dated operating record.

| Area | Team responsibility | Dependency or failure effect | Evidence needed for less dependence |
| --- | --- | --- | --- |
| Storage | Provider account, upload admission and storage ledger | Uploads and allowance changes depend on admission; reads also depend on the provider remaining available and paid | Independently operated storage and recovery drills |
| Public records | One publisher, public-read bucket and same-host mirror | Delayed or unavailable records can prevent fresh history checks; the mirror is not independent redundancy | Independent publication and retrieval demonstrated |
| Sign-up | Email verification, proof-of-work admission and mint binding | New sponsored identities depend on this service; it sees submitted verification data | A separately operated admission path meeting the same checks |
| Plans and billing | Payment account and signed entitlements | Purchases, renewals and entitlement changes depend on these services | Qualified production custody and documented recovery |
| Network authorities | Operator roster, registry and treasury keys | Compromise or mistakes can affect admission, spending and operator treatment | Production key ceremony and tested authority recovery |
| Operator programme | Revenue-funded alpha purchases, audited repayment and published allotments | Funding, liquidity and claim processing can limit repayments | Launch two-of-three signing, independent cost audit and reconciled public ledgers |
| Releases and website | Build publication, desktop signing and website hosting | Users depend on authentic downloads and the update channel | Verified release provenance, platform signing and recovery checks |

## Limits of those powers

These services do not receive private-message decryption keys through normal operation, and the team cannot authorise a spend of a user's identity without that user's keys. Operators still see metadata and may withhold service. A compromised client release or user device is a separate threat.

An accepted anchor cannot simply be edited by a storage operator. Retrieving its message body and checking its history still requires the relevant data and verification dependencies. See [What others can see](../security-and-privacy/what-others-can-see.md).

## Keeping the inventory current

Remove a dependency only after a working alternative has been demonstrated. Changes to control, custody or availability belong here and in the dated status record. Questions about these dependencies can be sent to [info@komms.app](mailto:info@komms.app).
