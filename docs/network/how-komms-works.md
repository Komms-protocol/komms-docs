# How Komms works

Devices encrypt and sign, operators deliver and store, Kaspa orders commitments, and Bittensor allocates rewards for measured service.

*Updated 22 October 2026*

> [!NOTE]
> This page describes the target architecture. [Network status](network-status.md) records what is operating; [What Komms runs](what-we-run.md) identifies team-controlled dependencies.

## The parts

| Part | Responsibility |
| --- | --- |
| Your device | Holds keys, encrypts private content and signs messages |
| Relay | Delivers signed envelopes before their identifiers are anchored |
| Index | Derives identity and anchor state from Kaspa and serves queries |
| Storage | Retains encrypted objects and history segments within their paid retention period |
| Kaspa | Orders identity transitions, governance and commitments to message identifiers |
| Bittensor | Allocates subnet emissions using validator weights |
| Komms Systems | Builds the apps and operates the launch services listed in the dependency inventory |

## Delivery and proof

Messages, replies, edits, reactions and moderation travel off chain. Relays deliver signed envelopes, allowing recipients to read a message before it is anchored. Later, an identity spend on Kaspa commits to a batch of identifiers.

Identity changes and private-conversation control events use the ordered control plane. Public governance and clear MLS handshakes can reveal membership, although private message bodies remain encrypted. See [Message delivery and anchoring](../security-and-privacy/delivery-and-anchoring.md) and [What others can see](../security-and-privacy/what-others-can-see.md).

## Identity and verification

An identity is held in a Kaspa covenant. Its owner and recovery keys authorise the relevant state transitions. Komms does not hold a key that grants control over a user's identity.

Verifiers reconstruct the history against the pinned template and node state. A successful live check requires an open author identity and the necessary records. Public-record availability still depends on the launch publisher and storage provider.

## Operators and incentives

Miners run a Kaspa node and the Komms capabilities they advertise. Validators derive their own chain view, probe miners and submit weights. The initial scoring stage is index-only; a planned capability receives no credit merely because an operator advertises it.

Native emissions reward scored work. Audited sponsored-fee repayment uses a separate operator-program alpha pot. The adopted funding policy allocates 25% of previous-month gross revenue to alpha purchases for that programme. These are distinct flows, and neither emissions nor repayment funding is guaranteed. See [Incentives and funding](incentives.md).

## Read further

- [Network status](network-status.md)
- [Evidence and claim boundaries](evidence.md)
- [Whitepaper and papers](papers.md)
- [Mining](../mining-and-validating/mining.md) and [validating](../mining-and-validating/validating.md)
