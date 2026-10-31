# Mining on Komms

What a Komms miner provides, how work is measured and what an operator must qualify before serving users.

*Updated 30 October 2026*

> [!NOTE]
> General onboarding is not open yet. The turnkey package is still being qualified with initial operators. Do not send funds or register a hotkey based on this guide. [Network status](../network/network-status.md) records readiness.

## The work

A miner runs a Kaspa node and Komms services. The architecture separates **indexing**, **storage** and **serving** so each capability can be measured. Proving and paid RPC are roadmap work.

The initial incentive stage scores index correctness. Storage and serving receive no score until their own probes and budgets are enabled and qualified. Running extra software is not, by itself, evidence of rewarded work.

Validators compare answers with their own Kaspa nodes and use bounded probes. A miner must provide correct data, persist required state and recover without silently losing accepted work.

## Rewards and costs

Bittensor emissions reward measured work according to validator weights and chain rules. The planned launch programme would separately audit sponsored Kaspa costs and repay accepted claims in alpha from an operator-program pot. Operating repayments have not been established. A probe stipend is also separate from customer demand. See [Incentives and funding](../network/incentives.md).

Emissions, alpha price, claim acceptance and liquidity are variable. Komms does not promise a fixed return, cost coverage or repayment from emissions. Operators need a spending limit, a funded Kaspa wallet and enough resources to remain online while claims are reviewed.

## What turnkey setup must cover

The release package must pin its source and binaries, verify prerequisites and explain every action before starting a spending service. It must support:

- A synced Kaspa node and verified network selection
- Hotkey registration and endpoint publication on the intended Bittensor network
- Explicit activation state, persistent index and broadcast data, and bounded sponsor spending
- Export of auditable sponsored-cost claims without exposing private keys
- Health checks, actionable logs, upgrades, restart and host-loss restoration

A binary being present is not an upgrade check. A fresh database starting successfully is not proof that the previous host's accepted work was restored. Qualification must exercise those cases.

Hardware requirements, firewall rules, supported systems and exact installation commands will be published with the qualified package. Kaspa node synchronisation can take hours; installation completion is not node readiness.

## Initial operators

Contact [info@komms.app](mailto:info@komms.app) with your operating experience and proposed host. Do not include seeds, keys or wallet files. The [subnet website](https://komms-landing-landing-page.up.railway.app/subnet.html) provides the project overview; it is not an installer or registration instruction.
