# Channels, messages and replies

How conversations work in Komms, from channels and threads of replies to edits, deletes, reactions and pins.

*Updated 21 October 2026*

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

Messages are delivered straight away, so you can send several in a row without waiting. Each message shows its delivery state, from **sent** to **delivered** and then **anchored**. See [Message delivery and anchoring](../security-and-privacy/delivery-and-anchoring.md) for what each state means.

## Message order

Komms keeps one agreed order for every conversation, based on when each person's messages were anchored on Kaspa. Messages you've already seen stay where they are on your screen; the agreed order never shuffles them around later.

## Deleting messages

- In a **public channel**, deleting a message stops it being served straight away, and operators then erase it from storage.
- In a **private conversation**, the delete is encrypted like everything else. Members' apps hide the message; operators can't read the delete, so they keep the encrypted copy for its normal retention period.

Nobody can delete a copy that someone already saved or screenshotted.

## Search

Search finds messages already loaded on your device. Search across your full local history is **coming soon**.

## Notifications

You're notified of new messages and mentions in conversations your device can read. Push notifications on phones arrive with the mobile apps, which are **coming soon**.
