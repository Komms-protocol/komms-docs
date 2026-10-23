# How Komms works

Your device encrypts, independent operators deliver and store, Kaspa keeps the order, and Bittensor subnet 27 pays the operators.

*Updated 22 October 2026*

Komms is built on open networks rather than one company's data centre. Each part has one job.

| Part | Its job |
| --- | --- |
| **Your device** | Encrypts and signs everything you send. Keeps your keys. |
| **Relays** | Deliver messages to everyone in a conversation, straight away. |
| **Storage** | Holds encrypted files and backups, starting with Hippius. |
| **Kaspa** | Records your identity and fingerprints of your messages, so their order and authorship can be checked. |
| **Bittensor subnet 27** | Recruits the operators who run relays, indexes and storage, checks their work, and pays them. |
| **Komms Systems** | The company: builds the apps, sells plans and runs the services listed in [What the team still runs](what-we-run.md). |

## Two lanes: fast delivery, slow proof

Komms keeps two lanes separate:

- **Messages, replies, edits, reactions and moderation** travel off-chain through relays, so they're instant. They reach Kaspa only as fingerprints, in batches. See [Message delivery and anchoring](../security-and-privacy/delivery-and-anchoring.md).
- **Identity changes and membership of private conversations** go on Kaspa itself, where everyone sees one agreed order.

## Your identity lives on Kaspa

Your account's identity is a small contract on the Kaspa network that only your keys can change. Komms can't take it over or edit it. Your history is a chain of anchors that anyone can check against that identity.

## Who runs the network

Operators run Komms services and are paid through [Bittensor subnet 27](https://taostats.io/subnets/27):

- **Miners** run a Kaspa node plus Komms services: indexing (tracking identities and anchors), storing, and relaying messages.
- **Validators** check miners' work against Kaspa, with test messages and spot checks, and set how rewards are shared.

A miner that sponsors an anchor pays the small Kaspa fee up front. At least a quarter of subscription revenue purchases subnet 27 alpha, and miners are repaid from that alpha at the cost of the fees they paid. The subnet's emissions are a separate reward for scored work. Paying customers fund the fee repayment. Emissions are not Komms revenue. See [Mining on Komms](../mining-and-validating/mining.md).

## Checking for yourself

Your app doesn't trust any single operator. It reads from more than one and checks the answers against Kaspa. A message only shows as **Verified** when your own node, or nodes run by two independent operators, agree.

## Going deeper

- [Whitepaper and papers](papers.md)
- [Roadmap](roadmap.md)
- [Network status](network-status.md)
