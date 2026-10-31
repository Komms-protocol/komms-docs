# Network status

The team's dated deployment account and the remaining public-beta gates.

*Reviewed 30 October 2026; deployment evidence last reviewed 21 October 2026; subnet control proof accepted 25 October 2026*

This is a manually maintained report. It does not report live uptime, revenue
or current chain metrics. [Evidence and claim boundaries](evidence.md) explains
what each kind of evidence establishes.

## Network identifiers

| Network | Identifier | Recorded role |
| --- | --- | --- |
| Kaspa testnet | Testnet 10 | Current Komms test environment |
| Bittensor testnet | Subnet 503 | Validator and miner qualification |
| Bittensor mainnet | Subnet 27 | Intended production subnet; investors hold the netuid 27 owner key |

A control proof was accepted on 25 October 2026. The Komms mechanism is not claimed to be operating on netuid 27. Ownership and the accepted proof do not establish weight publication or operator payments.
The recorded 18-19 October chain observations still carried the previous Orion
identity. Check [Taostats](https://taostats.io/subnets/27/) for its current
chain presentation; no live metrics are copied into this report.

## Current operating stage

- The recorded Komms deployment runs on Kaspa TN10, with a team-run testnet
  validator on Bittensor subnet 503.
- The launch build is under integration. Merged code has not established a
  deployed v4 service or a public-beta release.
- Current incentive qualification is index-first. Required store, serve and
  v4 relay probes need separate activation and acceptance evidence.
- General miner and validator onboarding is not open. A first operator group
  is helping qualify the installation and scored-state journeys.
- Team and Community plans payable by card or KAS are **available soon**,
  following the 20 October 2026 catalog amendment. Nothing is purchasable yet.
  This repository does not report subscriptions sold, customer revenue or
  operator repayments. See [Plans and pricing](../getting-started/plans-and-pricing.md).
- Storage evidence is a Komms-managed Hippius account and a same-host mirror.
  Relay operation is team-run testnet work; independent storage and relay
  operation are not qualified.

## Public-beta acceptance

Launch acceptance includes the integrated messaging journey, a verified
release, three independently operated miners and a second independently run
validator. It also includes cost and scoring evidence, host-loss and restore
journeys, and working alerts. There is no fixed calendar soak.

Miner installation alone does not establish admission or useful work. A
returning or new operator must recover the required history and agree with the
reference state; starting an empty DB at a pruned node is not proof of that.
See [Mining](../mining-and-validating/mining.md).

## Kaspa mainnet

A mainnet public beta requires the necessary covenant functionality to be
active on Kaspa mainnet and Komms' exact anchor-shaped transaction to be
standard, accepted and mined. Production templates, custody and the
mainnet user journey must also pass. A testnet public beta is the alternative
if those gates are not met; this report does not claim that beta is live.

## Updates

Update this page when a deployment, independent qualification or public launch
is evidenced. Product guides describe the planned public-beta experience;
roadmaps describe later work. Send corrections or evidence requests to
[info@komms.app](mailto:info@komms.app).
