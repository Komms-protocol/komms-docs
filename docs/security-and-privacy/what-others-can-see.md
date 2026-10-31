# What others can see

The information visible to members, network operators and services in the public-beta design.

*Updated 22 October 2026*

> [!NOTE]
> This is the design's privacy boundary. See [Network status](../network/network-status.md) for deployment status. Encryption protects private content; it does not hide all membership or activity information.

## Observer boundaries

| Observer | Information available |
| --- | --- |
| Kaspa observer | Identity existence and transitions, anchor counts, identifiers and timing; public governance and clear MLS handshakes can reveal participants' covenant identities |
| Relay operator | Author and conversation identifiers, routing, preceding message identifier, type, size, timing and ciphertext |
| Index operator | Identity and anchor history, governance and handshake records, and the queries it serves |
| Storage provider | Stored objects, their sizes and access timing; private-content objects are encrypted |
| Upload front | IP address, connection metadata and byte counts; a TLS pass-through front does not read the encrypted HTTP body, but a service terminating TLS can |
| Public Kaspa node queried | Requesting IP address and queried addresses or state, unless the requester adds its own network privacy protection |
| Admitted operator or validator | Clear headers and ciphertext fetched for audit or replication; knowing a direct-message or group identifier can permit by-identifier retrieval until a member-only read gate exists |
| Conversation member | Content and metadata received while authorised; copies can survive removal or deletion |
| Public-records reader | Identity records, anchor counts and identifiers, and published state needed for verification |
| Komms storage ledger | Object identifiers, length, storage class and pool, claiming identity, signed claim, blinded conversation tag, upload identifier, claim/expiry/release times and release reason; workspace pools also identify their creator |
| Sign-up verification service | Submitted email, proof-of-work and verification data, timing and the attestation that binds admission to a mint |

Operators do not receive private-message decryption keys through these read paths. Ciphertext access still reveals metadata and enables traffic analysis; it is not equivalent to a member-only access policy.

## Conversation membership

A random conversation identifier does not encode its members. It also does not make membership secret: handshakes and public governance can link identities to that identifier. Do not use Komms on the assumption that private conversation membership is hidden from network observers.

## Public content and deletion

Anyone can read and copy a public channel. A valid deletion stops serving the affected content, followed by asynchronous deletion of eligible stored copies. An object with another live storage claim can remain stored. Komms cannot establish that every provider or recipient has physically erased every copy.

Private-message deletion is encrypted. Members' clients can hide the message, while operators retain ciphertext according to retention policy. Public anchor identifiers remain. See [Files and storage](../using-komms/files-and-storage.md).

## Public records and availability

The launch design has one Komms-run publisher and a public-read storage bucket, with a same-host mirror. That mirror is not an independent availability guarantee. Records remain available while the provider is paid; they contain no private-message plaintext but can expose the metadata listed above.

## Retention and website data

The storage-ledger policy removes identity fields 30 days after object deletion. This is a retention policy, not proof that every underlying copy has been erased.

The [Privacy notice](privacy-notice.md) separately covers the website's sign-up form, provider logs and other website data handling.
