# Validating on Komms

How validators check service and what independent operation must demonstrate.

*Updated 22 October 2026*

> [!NOTE]
> General validator onboarding is not open yet. The initial mechanism and operator package still need qualification. See [Network status](../network/network-status.md).

## Validator responsibilities

Validators derive a chain view from their own Kaspa node, probe miner capabilities, audit sponsored costs and publish Bittensor weights. They do not serve ordinary user requests.

The initial scoring stage is index-only. Storage, serving and later proving require their own qualified probes before receiving credit. Claims of measured work need reproducible inputs, probe results and the resulting weights.

A cost auditor must compare a claim with node-derived transactions, fees, eligibility and limits. The claimant's own ledger is not sufficient independent evidence.

## Independence and influence

Launch requires a second, independently operated validator. Common-control declarations and separate hosts help review ownership, but neither proves independence by itself.

A validator must not score a miner it controls. Operating keys, node access, administration and scoring must be separated in practice. Bittensor's stake and weight rules still determine each validator's influence; adding a second validator does not guarantee balanced power or prevent collusion.

## Before publishing weights

The release must identify the intended network and subnet, reproduce scores from recorded inputs, bound sponsorship and stipend budgets, handle unavailable or dishonest miners and show how operators recover after interruption. Weight publication must be explicitly enabled after those checks; ordinary installation should not publish it.

## Get involved

Contact [info@komms.app](mailto:info@komms.app) with your validator experience and proposed independent operating arrangement. Do not send private key material. Read [Incentives and funding](../network/incentives.md) and [What Komms runs](../network/what-we-run.md) before committing resources.
