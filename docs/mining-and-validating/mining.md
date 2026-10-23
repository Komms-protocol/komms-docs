# Mining on Komms

What Komms miners do on Bittensor subnet 27, how they're scored and paid, and how to join the waitlist while onboarding opens.

*Updated 22 October 2026*

> [!NOTE]
> **Coming soon.** We'll be releasing the miner onboarding process soon. We're onboarding a small first group of miners to test the set-up end to end before we publish the guide. **[Join the miner waitlist](https://komms.app/?intent=miner&src=docs-mining#start)** and we'll tell you as soon as it opens.

## What miners do

A Komms miner runs a Kaspa node and Komms services, in one or more roles:

| Role | What it does |
| --- | --- |
| Index | Follows Kaspa, tracks every Komms identity and anchor, and serves verified history |
| Store | Holds encrypted messages, history backups and files, and proves it still has them |
| Serve | Relays messages between people, and sponsors their anchors on Kaspa |

## How miners are scored

Validators test miners continuously against what Kaspa says is true:

- **Correctness:** answers must match the chain.
- **Availability:** stored data must be there when it's asked for, within a deadline.
- **Delivery:** test messages must arrive, in order, and be settled.
- **Honest sponsorship:** every anchor a miner sponsors is audited from chain data.

Failing a critical check can't be made up for by doing well on another. Message volume, fees and a miner's KAS balance are never part of the score. New roles are scored only once their tests are switched on, and the miner docs will say which stage is live.

## How miners are paid

- **Fee repayment.** A miner that sponsors anchors pays the Kaspa fees up front. At least a quarter of subscription revenue purchases subnet 27 alpha, and miners are repaid from that alpha at the cost of those fees, against a published ledger.
- **Rewards** come from subnet 27 emissions, shared according to validators' scores. That reward is separate from fee repayment. Emissions are not Komms revenue.
- **What is live.** Scoring has been run on the Bittensor test network. This page does not claim that registering on subnet 27 today earns Komms rewards. The launch requirement is on [Network status](../network/network-status.md).

## What you'll need

Hardware and set-up details will be published with the guide. Expect a Linux server able to run a Kaspa node, with a static IP.

## Get notified

**[Join the miner waitlist](https://komms.app/?intent=miner&src=docs-mining#start)**. Subnet 27 on Taostats: [taostats.io/subnets/27](https://taostats.io/subnets/27).
