# Export your history

Download a complete copy of your conversations that you, or anyone you share it with, can check against the Kaspa network.

*Updated 21 October 2026*

You can export everything your app holds, on any plan, at any time, including when a plan has lapsed.

## What's in an export

- Your messages, and the messages of others that your device holds
- The records that tie each person's messages to their anchors on Kaspa
- The result of checking each item

## Checking an export

An export can be checked offline, to confirm nothing in it was changed. With access to the Kaspa network (your own node, or nodes run by two independent operators), it can also be checked against each author's live identity.

Each item carries one of these results:

| Result | Meaning |
| --- | --- |
| Verified | Confirmed by your own node or by two independent operators |
| Single node | Confirmed by one node only, a weaker result |
| Cannot check | The network couldn't be reached to check it |
| Not found | No matching record was found |
| Failed | The records don't add up: the identity's first record was rejected, its history is broken, or the key isn't tied to a live identity |

A check proves who signed a message and its place in the author's history. It doesn't prove the exact time it was sent, which device sent it, or that the person holding the key was its rightful owner.

## Backups of your history

Komms backs up your history by default, encrypted with a key that comes from your recovery kit. That means you can get your history back on a new device. It also means that someone who steals your recovery kit could open that backup. See [Your recovery kit](../security-and-privacy/recovery-kit.md).

Workspace and server admins can set a backup policy for their conversations, and the apps follow it.

## What an export can't do

- Bring back files that were already removed after a plan lapsed
- Restore messages that no device of yours ever received
- Erase copies held by other people
