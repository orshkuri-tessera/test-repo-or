---
title: How integrations work
excerpt: What happens when you connect a tool to Arch.
hidden: false
---
<Callout icon="⚠️" theme="warn">
  This page is placeholder content for the docs prototype. Review it before you publish it to customers.
</Callout>

## Connections

A connection links one account in a vendor's product to your Arch organization. You create it in the Arch console from **Integrations**. Each connection holds the credential Arch uses and the settings you chose.

## What Arch needs from you

- An account in the vendor's product with permission to create API credentials.
- A read-only credential. Arch never needs write access to your tools.
- The region or URL of your vendor tenant, when the vendor runs more than one.

## Syncs

After you connect a tool, Arch runs a first sync. Later syncs run on a schedule. The connection page shows when the last sync finished and whether it succeeded.

## When a connection fails

The connection page shows the reason. Each integration guide has a **Troubleshooting** section that lists the common reasons and their fixes.
