# Roles and moderation

Give people the right permissions, keep conversations on track, and understand how moderation decisions take effect.

*Updated 22 October 2026*

> [!NOTE]
> This guide describes the planned public beta. See [Network status](../network/network-status.md) for availability and qualification.

Roles decide who can do what in a workspace or server. Moderation tools keep conversations healthy.

## Roles

| Role | Can |
| --- | --- |
| Admin | Manage the workspace or server, its channels, roles, members and plan |
| Moderator | Remove any message, pin and unpin, remove or ban members |
| Member | Read and post in the channels they belong to |
| Viewer | Read without posting |

Roles, moderation and the admin console come with **Team, Growth and Scale** for workspaces. Community servers include moderation tools.

## Moderation actions

- **Delete any message:** clients apply the signed deletion to new views. A message already displayed can remain visible with a label; this does not recall saved copies.
- **Pin and unpin:** keep important messages at the top of a channel.
- **Remove or ban:** clients enforce the signed authority change when received and validated. Offline devices cannot be updated immediately.
- **Channel restrictions**, such as read-only mode, have a five-hour canonical grace period in the launch design. Their display can update earlier; history acceptance follows the protocol rule.

## How decisions are recorded

Moderation actions are signed by the moderator and recorded like messages. Every member's app works out the same result from the same history, so there's no hidden "admin override" on a server somewhere.

A message someone has already seen is never silently erased from their screen by a later decision. It stays visible and is labelled.

## Private channels and bans

When someone is removed from a private channel or group, its encryption keys change. They keep anything they already received. Subsequent keys exclude them, subject to the ended-epoch delivery window and propagation limits described in [How encryption works](../security-and-privacy/how-encryption-works.md).
