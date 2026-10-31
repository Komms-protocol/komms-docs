# Evidence and claim boundaries

Use this page to distinguish a design commitment, a reported test result and
an operating service.

*Updated 30 October 2026*

## Reading the evidence

| Description | What it establishes |
| --- | --- |
| Specified or planned | A design or product requirement exists |
| Implemented | Code exists; this does not establish deployment or independent operation |
| Tested | The named test passed within its stated environment and limits |
| Deployed | A particular build was observed running in the named environment |
| Independently qualified | Separate operators reproduced the relevant journeys and failure/recovery outcomes |

[Network status](network-status.md) is the dated deployment account. It is
maintained by the team and is not a live uptime monitor or an independent
attestation. The whitepaper's evidence register is also a team-published
account; the repository does not contain the complete engineering logs needed
to reproduce its results.

## Public technical references

- [MLS, RFC 9420](https://www.rfc-editor.org/rfc/rfc9420): the group messaging
  protocol Komms uses. A standard's security properties do not by themselves
  establish that an application's integration is correct.
- [X-Wing specification](https://datatracker.ietf.org/doc/draft-connolly-cfrg-xwing-kem/):
  the hybrid key-encapsulation construction used for direct-message key exchange.
  Komms signatures remain classical.
- [Bittensor documentation](https://docs.learnbittensor.org/): the substrate
  governing registration, validation and native rewards. These rules can change;
  a dated paper is not a current chain-state observation.
- [Kaspa](https://kaspa.org/): the ordering and identity substrate. Mainnet
  acceptance of Komms' exact transaction shapes remains a release gate.
- [Subnet 27 on Taostats](https://taostats.io/subnets/27/): a public third-party
  chain view. Its network metrics do not prove Komms product availability.

## Security scope

Private direct messages, groups and private channels have testnet encryption
evidence; public channels are readable. Membership and traffic metadata have
separate exposure. Direct-message key exchange has testnet evidence of hybrid post-quantum
protection, while signatures remain classical. Recovery of identity control
and restoration of message history are different operations.

Read [How encryption works](../security-and-privacy/how-encryption-works.md),
[What others can see](../security-and-privacy/what-others-can-see.md) and
[Your recovery kit](../security-and-privacy/recovery-kit.md) for those limits.
The presence of audited or formally verified library components is not an
independent audit of Komms. This repository makes no certification or uptime
claim.

## Availability and verification

Independent history verification is planned, not available. It would need the message, supporting records, the
accepted template and node access while the author's identity remains open.
A fresh check after closure cannot establish the old history; an earlier
recorded result remains a local observation.

The public records store is proposed, not operating. Its planned availability
would depend on Komms continuing to pay the storage provider. Public-record
retrieval awaits qualification, including a credential-free read probe.
A same-host mirror would not establish independent availability. Storage retention, provider
deletion and restoration after operator loss need operational evidence, even
when the corresponding code has passed tests.

## Reviewing a paper

[Papers](papers.md) records the scope and version of each download. This
snapshot does not include a published checksum manifest. A checksum would
identify exact bytes, not establish that a technical or economic claim is correct.
Later roadmap phases are conditional plans, not release commitments.

For source-level review material, a missing evidence link or a disputed claim,
contact [info@komms.app](mailto:info@komms.app). Corrections should update the
canonical page and its date rather than leave contradictory accounts.
