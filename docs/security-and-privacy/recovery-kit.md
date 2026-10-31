# Your recovery kit

What the kit controls, how it differs from a history backup, and what to do if it is lost or exposed.

*Updated 30 October 2026*

> [!NOTE]
> This guide describes the public-beta recovery design. Recovery onto a new master seed is planned, not shipped; the procedures below are design descriptions, not available client instructions. See [Network status](../network/network-status.md) for availability and qualification.

The recovery kit contains your identity's recovery secret, covenant identifier and template version. The secret is generated independently of the device's master seed. Komms does not hold a copy.

> [!WARNING]
> Anyone holding the kit can immediately replace the identity's owner key or close the identity. This grants authority over the identity and its covenant value, not the separate wallet balance. The kit alone does not restore or control wallet funds. There is no protective waiting period for use of the kit.

## Keep it safe

- Keep an offline copy, or use a password manager you trust.
- Keep a copy separate from the device you use for Komms.
- Never send it in a chat, email or support request. Enter it only in the trusted account-recovery flow.

## Account control and old history

On a new device, a synced passkey may restore access to your encrypted seed vault, depending on the device and passkey provider. Check that your history and keys have actually been restored before discarding another device.

The planned recovery flow would restore **identity control** onto a new master seed if every device is lost. That flow is not shipped. It cannot recover old history by itself. Old backups still need their old archive key, derived from the old master seed, and the backup bytes must remain available within their retention period.

Full private-history [export](../using-komms/export-your-history.md) is planned, not available; retain existing devices, keys and backup data needed for important history. Identity recovery, backup restoration and export verification are different operations.

## Lost kit, signed-in device available

The design allows a signed-in owner to propose a replacement kit. Confirmation requires the recovery ticket to reach the protocol's 14-day delay. The device warns other signed-in devices of the proposal.

Replacement needs a deposit, returned on confirmation, and user-paid network fees. The holder of the old kit can still recover the identity during the delay. The delay protects against an unauthorised replacement proposal; it does not protect an exposed kit.

## Exposed kit or compromised device

If your master seed is exposed, create a new identity with a new master seed until fresh-seed recovery is released and qualified. Rotating to another key derived from the exposed seed is insufficient to remove the attacker's access.

For an exposed recovery kit, the planned procedure allows immediate replacement of the recovery key using both the current kit and owner key. Replacing the recovery key alone does not resolve an exposed master seed.

These are sensitive account operations. Do not rely on the planned fresh-seed recovery flow until it is released and qualified. [Contact Komms](mailto:info@komms.app) for help, without sending any secret material.

## Recovery costs

The launch policy sponsors one recovery per identity in 30 days. Further recoveries and lost-kit replacement are user-paid. Sponsorship does not remove the need for a valid signature or make old backups decryptable.
