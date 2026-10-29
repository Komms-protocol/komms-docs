# FAQ

Short answers to the questions people ask most about Komms.

*Updated 22 October 2026*

> [!NOTE]
> This guide describes the planned public beta. See [Network status](../network/network-status.md) for availability and qualification.

## Do my staff or members need crypto?

No. People sign in with a passkey and use Komms like any chat app. Komms covers the network costs of everyday use, so nobody needs to buy or hold KAS. A [wallet](../using-komms/wallet.md) is built in for those who want one.

## Is it really end-to-end encrypted?

Private channels, direct messages and group chats are end-to-end encrypted: only their members can read them. Public channels in community servers are readable by anyone, by design. See [How encryption works](../security-and-privacy/how-encryption-works.md).

## Where is my data stored?

Files are encrypted and stored with independent storage providers, starting with Hippius. Messages are relayed by independent operators. Kaspa holds proof of the order of events, not the messages themselves. See [How Komms works](../network/how-komms-works.md).

## Is there a per-seat fee or a member limit?

Neither. You pay one price per workspace or server. Plans recommend a team size but don't limit it. See [Plans and pricing](plans-and-pricing.md).

## Can I pay monthly?

Yes. Every paid plan can be paid yearly or monthly. Yearly saves about 17%.

## Is there a mobile app?

Komms launches on the web and as desktop apps for macOS and Windows. iOS and Android apps with push notifications are **coming soon**. See [Apps](../using-komms/apps.md).

## Are there voice and video calls?

Voice and video calls, end-to-end encrypted, are **coming soon**.

## What does "anchored" mean on a message?

Delivery and anchoring are separate. An accepted anchor commits to message identifiers on Kaspa. Checking a message then requires the relevant identity records, template and node state; the author must remain open for a fresh live check. See [Message delivery and anchoring](../security-and-privacy/delivery-and-anchoring.md).

## What happens if I lose my phone?

A synced passkey may restore your seed vault, depending on your devices and provider. The [recovery kit](../security-and-privacy/recovery-kit.md) can restore identity control, but the kit alone cannot decrypt old history. That needs its old archive key and retained backup data.

## What happens if Komms shuts down?

Your identity lives on Kaspa, not in a Komms database, and you can keep a verifiable [export of your history](../using-komms/export-your-history.md). Some services are still run by the Komms team at launch, and those would be affected. See [What Komms runs today](../network/what-we-run.md).

## Can I move my community from Discord or Telegram?

There's no automatic import at launch. On the Large communities plan, we help you plan and run the move.

## Is Komms on mainnet?

The recorded Komms deployment uses Kaspa Testnet 10 and Bittensor testnet subnet 503. Bittensor mainnet subnet 27 is the intended production slot; ownership does not establish that the Komms mechanism is qualified and operating there. See [Network status](../network/network-status.md) for where things stand.

## How do I contact you?

Email [info@komms.app](mailto:info@komms.app).
