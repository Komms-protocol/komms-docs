# Message delivery and anchoring

How fast delivery differs from a later, verifiable commitment on Kaspa.

*Updated 30 October 2026*

> [!NOTE]
> This guide describes the public-beta design, not a measured production latency or availability promise. See [Network status](../network/network-status.md).

**Delivery** passes a signed message through relays to recipients. **Anchoring** records a commitment to a batch of message identifiers in a Kaspa transaction. Private message bodies stay off chain.

Delivery can happen before anchoring. A relay's acknowledgement does not establish that a recipient read the message, or that its identifier has been accepted on Kaspa. The launch mechanism has no universal recipient-delivery receipt.

## Reading the states

| State | Meaning |
| --- | --- |
| Sent | The app submitted the message to its relays |
| Received on this device | This device received the envelope; it does not establish delivery to every recipient |
| Anchor pending | The identifier is awaiting an accepted anchor |
| Anchored | The identifier is included in an accepted Kaspa anchor |

Independent verification is a planned capability, not an available client result. The following labels describe its intended outcomes. **Verified** requires checking with your own node, or nodes run by two independent operators. **Single node** records a weaker observation. Neither label proves who physically held the signing key.

## Sponsorship and waiting

The base launch policy allows a sponsored anchor on a four-hour gap, with a bounded allowance for additional sponsored spends inside that gap. Membership, key or moderation changes can consume that allowance. They do not all receive an unlimited fee exemption.

If the allowance is exhausted, the app must wait or offer a user-paid transaction through the [wallet](../using-komms/wallet.md). Actual acceptance also depends on node policy, block capacity, fees and connectivity. The four-hour gap is a policy, not a deadline guarantee.

A sponsored batch holds at most 100 identifiers, including any history-segment identifier. Relays also bound unanchored traffic. Reaching a bound can delay further delivery or require an anchor; it does not establish that all pending messages are durable.

A lost device, abandoned pending batch or key superseded before anchoring can leave a delivered message outside canonical history. Keep recovery and [backup](recovery-kit.md) limits in mind.

## Agreed order

The canonical history uses Kaspa's accepted anchor order and the message relationships defined by the protocol. It does not trust device clocks. The app can preserve the order already displayed to a reader; that display order is separate from a later canonical check.

## What verification requires

A fresh check needs the message, the required identity and anchor records, the pinned covenant template and access to the appropriate node state. The author's identity must remain open for the live-identity check. A closed lineage cannot receive a fresh successful live check under this model.

A saved earlier verification result remains a record of what that verifier observed then. It is not a new network observation. See [Export your history](../using-komms/export-your-history.md).

Anchoring establishes the signed commitment and its place in an identity's history. It does not establish the exact send time, delivery, which device signed, or that its key holder was the rightful owner.
