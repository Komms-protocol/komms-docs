# What others can see

Exactly what the Kaspa network, operators, storage providers, Komms and other members can and can't learn.

*Updated 21 October 2026*

Encryption hides what you say in private conversations. Some information about your activity is still visible to the people and systems that make Komms work. Here's who can see what.

| Who | Can see | Can't see |
| --- | --- | --- |
| Anyone looking at Kaspa | That your identity exists; how many messages you anchored, and when; fingerprints of those messages | Message content, who you wrote to, which conversations |
| Relay operators | That your account sent something to a conversation, its size and when | Content of private messages |
| Storage providers | Encrypted files, their size and when they were stored | File contents in private conversations |
| Komms (storage records) | Which workspace or person each stored file is charged to, its size and type of storage | File contents in private conversations |
| Komms (sign-up checks) | Your email address, used to check your sign-up | Your messages |
| Members of a conversation | Everything sent in it after they joined | Private conversations they're not in |
| Anyone | Everything in a public channel | Private channels, direct messages, group chats |

## Public channels

Public channels in community servers are open by design. Anyone with the link can read them, and anything posted there can be copied. Deleting a public post stops it being served and removes stored copies, but can't recall copies people already took.

## Conversation IDs

Every conversation has a random ID, so nobody can work out who is talking to whom from the ID alone.

## Public records

For every identity, a small set of public records is kept so that anyone can check its history: the count and fingerprints of each anchor, the identity's current state and its first record. They contain no message content.

## Copies other people hold

Nothing in Komms can stop someone in a conversation saving, forwarding or screenshotting what they receive. Treat a message like anything else you send to another person.

For the website's own data handling (the sign-up form, server logs), see the [Privacy notice](privacy-notice.md).
