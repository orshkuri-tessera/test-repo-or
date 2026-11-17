---
title: Example EDR
excerpt: Connect an Example EDR tenant to Arch. Mock guide for the docs prototype.
hidden: false
---
<Callout icon="⚠️" theme="warn">
  **Mock guide.** Example EDR is not a real product. This page shows the structure and components every integration guide uses. Copy `templates/integration-guide.md` to write a real one.
</Callout>

Arch reads your endpoints, their operating systems and their protection status from Example EDR.

## Before you start

You need:

- An Example EDR account with the **Super Admin** role.
- Your Example EDR region: **US**, **EU** or **APAC**.

Arch needs these read-only permissions:

| Permission       | Why Arch needs it                                     |
| :--------------- | :---------------------------------------------------- |
| `endpoints:read` | Lists your computers and servers                      |
| `policies:read`  | Shows which protection policy applies to each endpoint |
| `tenant:read`    | Confirms the region and tenant ID                     |

## Create an API credential in Example EDR

1. In the Example EDR console, go to **Settings** > **API credentials**.
2. Click **Add credential**. Name it `Arch`, and select the **Read only** role.
3. Copy the **Client ID** and **Client secret**. Example EDR shows the secret once.

<Callout icon="📘" theme="info">
  If you lose the secret, delete the credential and create a new one.
</Callout>

{/* Replace with a real screenshot: <Image src="..." alt="..." /> */}

## Connect Example EDR in Arch

1. In the Arch console, go to **Integrations**, find **Example EDR**, and click **Connect**.
2. Paste the **Client ID** and **Client secret**, and select your region.
3. Click **Test**. Arch checks that the credential works and has the permissions above. When the test passes, click **Save**.

Arch starts the first sync right away. A first sync usually finishes within an hour.

## What Arch collects

| Data                         | Shown in Arch as |
| :--------------------------- | :--------------- |
| Computers and servers        | Assets           |
| Operating system and version | Asset details    |
| Protection status            | Asset details    |

Arch does not collect files, process data or alerts from Example EDR.

## Troubleshooting

<Accordion title="The test fails with &quot;Invalid credential&quot;" icon="fa-circle-exclamation">
  The client ID or secret is wrong, or the credential was deleted. Create a new credential and enter it again.
</Accordion>

<Accordion title="The test fails with &quot;Missing permission&quot;" icon="fa-circle-exclamation">
  The credential does not have the **Read only** role. Edit the credential in Example EDR and change its role.
</Accordion>

<Accordion title="The sync finished but shows no assets" icon="fa-circle-exclamation">
  Check the region. A credential from the EU region returns no endpoints when you select US.
</Accordion>

## Disconnect

In the Arch console, open the connection and click **Disconnect**. Then delete the `Arch` credential in Example EDR.
