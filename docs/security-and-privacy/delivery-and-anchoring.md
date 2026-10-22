# Message delivery and anchoring

Messages arrive instantly. A few hours later they're anchored on Kaspa, so anyone can check who sent what, and in what order.

*Updated 21 October 2026*

Komms separates **delivering** a message from **proving** it.

- **Delivery** is instant. Operators called relays pass your message to the other people in the conversation, usually in under a second.
- **Anchoring** comes later. Your app records a fingerprint of your recent messages in one transaction on the Kaspa network. After that, anyone can check that you sent them and where they sit in the conversation.

Message content never goes on the blockchain, only fingerprints.

## Delivery states

| State | Meaning |
| --- | --- |
| Sent | Your app has sent the message to the conversation's relays |
| Delivered | It reached the other people's apps |
| Anchor pending | It's waiting for your next anchor |
| Anchored | Its fingerprint is recorded on Kaspa and confirmed |

Messages also show whether they could be checked: **Verified** when confirmed by your own node or by two independent operators, or **Single node** when only one node confirmed it, which is a weaker result.

## How often messages are anchored

At launch, each account anchors about **every 4 hours** while the app is open. Komms covers the network fee, through the operator who sponsors the anchor.

Some things are anchored straight away, without waiting:

- joining a private conversation
- leaving one, changing role or changing keys
- moderation actions
- reaching the limit of messages waiting to be anchored

If you hold KAS in your [wallet](../using-komms/wallet.md), you can pay for an anchor yourself at any time.

## The waiting limit

Up to **100 messages** per person can wait for an anchor. If you reach the limit, your app anchors early and tells you. No message is lost.

To stop spam, the people you write to see at most 100 of your unanchored messages in any 48 hours. Anything beyond that is held until it's anchored.

## The agreed order

Messages from different people are put in order by when their anchors were accepted on Kaspa, not by the clocks on their devices. Messages you've already seen stay where they are on your screen; the agreed order never re-sorts them.

## What anchoring proves, and what it doesn't

Anchoring proves that your identity's key approved a batch of messages, and their order in your history. It doesn't prove exactly when a message was sent, that it was delivered, which of your devices sent it, or that the person holding the key was its rightful owner.
