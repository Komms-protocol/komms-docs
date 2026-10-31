# What others can see

The information visible on testnet today and the planned public-beta privacy boundary.

*Updated 30 October 2026*

> [!NOTE]
> The table below describes the planned privacy boundary. On testnet today, stored objects can be retrieved anonymously by content ID; the planned signed-request policy is not the current access boundary. See [Network status](../network/network-status.md) for deployment status. Encryption protects private content; it does not hide all membership or activity information.

## Observer boundaries

| Observer | Information available |
| --- | --- |
| Kaspa observer | Identity existence and transitions, anchor counts, identifiers and timing; public governance and clear MLS handshakes can reveal participants' covenant identities |
| Relay operator | Author and conversation identifiers, routing, preceding message identifier, type, size, timing and ciphertext |
| Index operator | Identity and anchor history, governance and handshake records, and the queries it serves |
| Storage provider | Stored objects, their sizes and access timing; private-content objects are encrypted |
| Upload front | IP address, connection metadata and byte counts; a TLS pass-through front does not read the encrypted HTTP body, but a service terminating TLS can |
| Public Kaspa node queried | Requesting IP address and queried addresses or state, unless the requester adds its own network privacy protection |
| Admitted operator or rostered validator | Clear headers and ciphertext fetched by signed request for audit or replication |
| Any admitted identity knowing a direct-message or group direct-message conversation ID | Ciphertext fetched by a signed request naming that conversation ID; a member-only read gate is not built |
| Conversation member | Content and metadata received while authorised; copies can survive removal or deletion |
| Public-records reader | Identity records, anchor counts and identifiers, and published state needed for verification |
| Komms storage ledger | Object identifiers, length, storage class and pool, claiming identity, signed claim, blinded conversation tag, upload identifier, claim/expiry/release times and release reason; workspace pools also identify their creator |
| Sign-up verification service | Submitted email, proof-of-work and verification data, timing and the attestation that binds admission to a mint |

Neither anonymous object retrieval today nor the planned signed-request paths give requesters private-message decryption keys. Ciphertext access still reveals metadata and enables traffic analysis; it is not equivalent to a member-only access policy.

## Conversation membership

A random conversation identifier does not encode its members. It also does not make membership secret: handshakes and public governance can link identities to that identifier. Do not use Komms on the assumption that private conversation membership is hidden from network observers.

## Public content and deletion

Anyone can read and copy a public channel. Under the planned deletion policy, a valid deletion would stop new serving of the affected content and schedule eligible stored copies for provider deletion. Another live storage claim could keep an object stored. Live deletion and sweeps lack operational evidence: a testnet deletion does not establish storage removal or cessation of anonymous content-ID retrieval. Komms cannot establish that every provider or recipient has physically erased every copy.

In the planned private-message deletion flow, the deletion would be encrypted and members' clients would hide the message; ciphertext would remain subject to the planned retention policy. This would not remove public anchor identifiers. See [Files and storage](../using-komms/files-and-storage.md).

## Public records and availability

The proposed public records store would use one Komms-run publisher, a public-read storage bucket and a same-host mirror. Retrieval still awaits qualification, including a credential-free read probe. Planned availability would depend on Komms continuing to pay the provider; the mirror would not establish independent availability. The proposed records would exclude private-message plaintext but expose the metadata listed above.

## Retention and website data

The planned storage-ledger policy calls for removing identity fields 30 days after object deletion. Live enforcement is unverified, and the policy would not prove that every underlying copy had been erased.

The [Privacy notice](privacy-notice.md) separately covers the website's sign-up form, provider logs and other website data handling.
