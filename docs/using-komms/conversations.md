# Channels, messages and replies

How conversations work in Komms, from channels and replies to edits, deletes, reactions and pins.

*Updated 30 October 2026*

> [!NOTE]
> This guide describes the planned public beta. See [Network status](../network/network-status.md) for availability and qualification.

Every conversation in Komms works the same way, whether it's a channel, a direct message or a group chat. The same tools are available everywhere.

## Kinds of conversation

| Kind | Who can read it | Encrypted |
| --- | --- | --- |
| Public channel | Anyone with the link | No, readable by design |
| Private channel | Its members | Yes, end to end |
| Direct message | The two of you | Yes, end to end |
| Group chat | Its members | Yes, end to end |

Public channels exist in community servers. Workspace channels are private.

## What you can do in any conversation

- **Send** messages and files
- **Reply** to a specific message
- **Edit** your own messages; an edited message shows that it changed
- **Delete** your own messages
- **React** with an emoji
- Moderators can also **delete any message** and **pin** or **unpin** messages. See [Roles and moderation](roles-and-moderation.md).

## Sending without waiting

The planned relay flow would let you send several messages before anchoring. It does not guarantee immediate delivery or a universal recipient-delivery receipt. The design distinguishes **sent**, **received on this device**, **anchor pending** and **anchored**. See [Message delivery and anchoring](../security-and-privacy/delivery-and-anchoring.md) for what each state means.

## Message order

Komms keeps one agreed order for every conversation, based on when each person's messages were anchored on Kaspa. Messages you've already seen stay where they are on your screen; the agreed order never shuffles them around later.

## Deleting messages

The following is the planned deletion policy. Live deletion and sweeps are not operationally evidenced; deleting on testnet does not establish storage removal or stop anonymous content-ID retrieval.

- In a **public channel**, an accepted deletion would stop new serving of the affected message and schedule eligible stored copies for asynchronous removal; another live storage claim could keep an object stored.
- In a **private conversation**, the delete is encrypted like everything else. Members' apps apply the deletion; operators cannot read it, so ciphertext remains subject to normal retention. A previously displayed message can remain labelled in that view.

Nobody can delete a copy that someone already saved or screenshotted.

## Search

Search finds messages already loaded on your device. Search across your full local history is **coming soon**.

## Notifications

You're notified of new messages and mentions in conversations your device can read. Push notifications on phones arrive with the mobile apps, which are **coming soon**.
