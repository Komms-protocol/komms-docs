# Incentives and funding

The launch design connects operator rewards to measured service and keeps
cost repayment separate from native Bittensor emissions.

*Updated 22 October 2026*

## Work that earns score

Validators use their own Kaspa node as the reference and run the probes
required by the active scoring stage. Those obligations include correctness,
retrieval and availability, then relay delivery and settlement as the relevant
services are qualified. A required probe that is disabled, stale or missing
blocks publication. Miner responses must carry the required signatures and
miners must be admitted through the signed operator roster.

Fees, sponsored volume, payment size, unsettled delivery and a miner's KAS
balance are not score inputs. Passing more traffic is not proof of useful work.
Capabilities earn score only after their measurements become required.

See [Network status](network-status.md) for the current index-first stage.

## Three separate accounts

| Flow | Basis | Launch design |
| --- | --- | --- |
| Native subnet rewards | Validator weights and Bittensor consensus | Reward measured service; do not reimburse a fee invoice |
| Cost repayment | Accepted on-chain spends and a signed operator claim | Pay eligible costs in alpha from the operator-program pot |
| Probe stipend | Required probes passed | Account separately from both weights and cost repayment |

Operators front sponsored Kaspa fees from their own wallets. The repayment
ledger includes accepted transactions, the applicable fee floor, eligibility
and the lane's allotment. A second signer recomputes it against an independent
node before the weekly payment batch. The operator signs a claim using its
registered claim key; its coldkey stays cold.

A spend outside the sponsorship policy or a lane's allowance is not eligible
merely because the operator paid it. Cost repayment is intended to cover
eligible cost, not to create a fee-based reward multiplier.

## Subscription funding

The adopted policy allocates 25% of the previous month's gross revenue to
operator-program alpha purchases. Purchased alpha, retained alpha, the
repayment pot and native subnet emissions are recorded separately. This
allocation is a planned funding policy, not evidence of current sales,
executed purchases or completed repayments.

At launch the planned repayment pot uses two-of-three signing. Public weekly
ledgers, independent recomputation, bounded funding and a claim/dispute process
are acceptance requirements. An automated claim contract is later work.

The [launch catalogue](../getting-started/plans-and-pricing.md) describes
planned subscriptions. Product demand, operating costs and the adequacy of the
programme budget still need measured evidence from independent operators.

## Admission and common control

The signed roster binds an operator's public identities, capabilities,
sponsor and claim keys, and reward group. Common-control declarations group
related operators so that copying a service does not create an independent
operator. Validators exclude miners declared under their own control.

These checks rely on reviewed declarations. A signed group label alone does
not prove independence or detect an undisclosed shared backend.

## Evidence required before activation

- A dated required probe set, current signatures and fresh successful journeys
- Independent operators with recorded control and costs
- Dry-run weights checked against the approved policy and fee budgets
- An accepted Bittensor publication followed by the matching revealed weights
- Tested ledger recomputation, claim handling, funding custody and recovery

Testnet qualification, mainnet weight publication and operating repayments are
separate milestones. None is inferred from a merged change or from ownership
of subnet 27. See [Evidence and claim boundaries](evidence.md).
