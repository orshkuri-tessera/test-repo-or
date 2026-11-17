# Arch integrations docs (ReadMe prototype)

This repo syncs to a [ReadMe](https://readme.com) docs site. Pages live in `docs/<Category>/<slug>.md`, and each folder's `_order.yaml` sets the sidebar order.

## Writing integration guides

- This site is customer-facing. Each integration guide is for the administrator who connects the tool.
- Start every guide from `templates/integration-guide.md`, then add its slug to the category's `_order.yaml`.
- "Integration": a tool Arch supports. "Connection": one customer account linked to Arch. Do not use "connector".
- Do not document internals: simulators, rate limits, sync mechanics, service names or code paths.
- Never name a customer or prospect.
- Use active voice and second person. Bold UI labels: click **Settings**.

## Check your changes

```sh
npx @readme/cli lint
```
