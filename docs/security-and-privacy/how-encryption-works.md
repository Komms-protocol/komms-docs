# How encryption works

What end-to-end encryption protects, where post-quantum protection applies, and what encryption cannot hide.

*Updated 30 October 2026*

> [!NOTE]
> This guide describes the public-beta design. See [Network status](../network/network-status.md) for what is running and what still needs qualification.

Private direct messages, groups and private channels have testnet encryption evidence. In the public-beta design, private messages and files are encrypted on members' devices before upload. Operators carry ciphertext; conversation members hold the keys that open it. Public channels are readable by design.

## What's encrypted

| Conversation | Protection |
| --- | --- |
| Direct messages | End-to-end encryption with hybrid post-quantum key exchange |
| Group chats and private channels | End-to-end encryption |
| Public channels | Readable by anyone |
| Files in private conversations | Encrypted on the sending device |

## Conversation keys

Komms uses **MLS**, Messaging Layer Security, for private conversations. [RFC 9420](https://www.rfc-editor.org/rfc/rfc9420) defines the standard. Membership changes advance the conversation's key state.

A new member receives keys for new messages. Removing a member changes the keys for subsequent messages, but does not erase anything they already received. Devices retain some earlier key state for a bounded period to handle delayed delivery. Removal and key erasure are not instantaneous across offline devices.

Messages also carry the author's signature. Checking that signature and its relationship to a Kaspa identity is separate from decrypting the message.

## Post-quantum protection

Direct messages use **X-Wing**, combining ML-KEM-768 with X25519. The hybrid protects direct-message confidentiality against an attacker who records encrypted traffic for later decryption, subject to the security of the construction and its implementation.

Kaspa transactions, message signatures and MLS credentials remain classically signed. The scoped claim is hybrid post-quantum **direct-message confidentiality**. It is not a claim that every part of Komms resists quantum attacks.

## Visible information

Encryption does not hide all communication metadata. Relays see routing, author identifiers, sizes and timing. Public governance records and MLS handshakes can reveal the covenant identities participating in a private conversation. Recipients can save, forward or screenshot plaintext.

[What others can see](what-others-can-see.md) lists these boundaries, including storage and sign-up records.

## Backups and recovery

History-backup keys derive from the device's **master seed**. The recovery kit contains a separate recovery secret and identity information. Recovery of identity control onto a new master seed is planned, not shipped. The kit alone cannot decrypt old history.

Restoring history requires the appropriate old seed or archive key and the retained backup data. A synced passkey is not, by itself, proof that those data and keys have been restored. See [Your recovery kit](recovery-kit.md) and [Export your history](../using-komms/export-your-history.md).
