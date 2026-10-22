# How encryption works

What end-to-end encryption protects in Komms, where post-quantum protection applies, and what encryption can't hide.

*Updated 21 October 2026*

Private conversations in Komms are end-to-end encrypted on your device. Messages and files are locked before they leave, and only the members of the conversation hold the keys to open them.

## What's encrypted

| Conversation | Encryption |
| --- | --- |
| Direct messages | End to end, with hybrid post-quantum key exchange |
| Group chats | End to end |
| Private channels | End to end |
| Public channels | None: readable by anyone, by design |
| Files in private conversations | Encrypted on your device before upload |

## How it works

Komms uses **MLS** (Messaging Layer Security, the open standard RFC 9420) for private conversations. Each conversation has its own keys, shared only between members' devices.

- When someone joins, they can read new messages from that point on.
- When someone leaves or is removed, the keys change, so they can't read anything sent afterwards.
- Old keys are destroyed after a short, set time, which limits what a stolen device could reveal about the past.

Every message is also **signed** with your identity's key, so recipients can check it really came from you and wasn't changed.

## Post-quantum protection, precisely

Direct messages use **X-Wing**, a hybrid key exchange that combines ML-KEM-768 (a post-quantum algorithm) with X25519. This protects them against "harvest now, decrypt later": someone recording encrypted traffic today and hoping to break it with a quantum computer later.

Signatures are not post-quantum. That covers Kaspa transactions, message signatures and the credentials inside MLS. So it would be wrong to say "Komms is post-quantum". The accurate claim is that direct-message **confidentiality** has hybrid post-quantum protection.

## What encryption can't hide

Encryption protects what you say. It doesn't hide everything about the fact that you're talking:

- Operators who relay messages can see that an account sent something to a conversation, and when.
- The Kaspa network shows how many messages each person anchored, and when, but not their content or recipients.
- Anyone in a conversation can copy, save or screenshot what they receive.

See [What others can see](what-others-can-see.md) for the full list.

## Backups and your recovery kit

Your history backup is encrypted with a key that comes from your recovery kit. That lets you restore your history on a new device. It also means that anyone who steals your recovery kit can open your backed-up history, even though messages in transit stay protected. See [Your recovery kit](recovery-kit.md).
