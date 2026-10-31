# FAQ

Short answers to the questions people ask most about Komms.

*Updated 30 October 2026*

> [!NOTE]
> This guide describes the planned public beta. See [Network status](../network/network-status.md) for availability and qualification.

## Do my staff or members need crypto?

No. People sign in with a passkey and use Komms like any chat app. Komms covers the network costs of everyday use, so nobody needs to buy or hold KAS. An optional built-in [wallet](../using-komms/wallet.md) is part of the public-beta design.

## Is it really end-to-end encrypted?

Private channels, direct messages and group chats have testnet end-to-end encryption evidence: only their members hold the content keys. Public channels in community servers are readable by anyone, by design. See [How encryption works](../security-and-privacy/how-encryption-works.md).

## Where is my data stored?

Private-conversation files are encrypted before storage. Current storage evidence is a Komms-managed Hippius account with a same-host mirror, and relay operation is team-run testnet work. Independent storage and relay operation are not qualified. Kaspa holds proof of the order of events, not the messages themselves. See [How Komms works](../network/how-komms-works.md).

## Is there a per-seat fee or a member limit?

Neither. You pay one price per workspace or server. Plans recommend a team size but don't limit it. See [Plans and pricing](plans-and-pricing.md).

## Can I pay monthly?

Yearly and monthly billing are planned, with yearly saving about 17%. Team and Community plans payable by card or KAS are **available soon**; nothing is purchasable yet.

## Is there a mobile app?

Web is the public-beta target. macOS and Windows desktop shells remain in flight, subject to signing and release qualification. iOS and Android apps with push notifications are **coming soon**. See [Apps](../using-komms/apps.md).

## Are there voice and video calls?

Voice and video calls, end-to-end encrypted, are **coming soon**.

## What does "anchored" mean on a message?

Delivery and anchoring are separate. An accepted anchor commits to message identifiers on Kaspa. Checking a message then requires the relevant identity records, template and node state; the author must remain open for a fresh live check. See [Message delivery and anchoring](../security-and-privacy/delivery-and-anchoring.md).

## What happens if I lose my phone?

A synced passkey may restore your seed vault, depending on your devices and provider. Recovery onto a new master seed using the [recovery kit](../security-and-privacy/recovery-kit.md) is planned, not shipped. The kit alone cannot decrypt old history. That needs its old archive key and retained backup data.

## What happens if Komms shuts down?

Your identity lives on Kaspa, not in a Komms database. Full private-history [export](../using-komms/export-your-history.md) is planned, not available. Current testnet services depend on the Komms team and its storage provider, so a shutdown could affect access. See [What Komms runs today](../network/what-we-run.md).

## Can I move my community from Discord or Telegram?

There's no automatic import at launch. On the Large communities plan, we help you plan and run the move.

## Is Komms on mainnet?

The recorded Komms deployment uses Kaspa Testnet 10 and Bittensor testnet subnet 503. Investors hold the Bittensor mainnet netuid 27 owner key, and a control proof was accepted on 25 October 2026. The Komms mechanism is not claimed to be operating there, publishing weights or paying operators. See [Network status](../network/network-status.md) for where things stand.

## How do I contact you?

Email [info@komms.app](mailto:info@komms.app).
