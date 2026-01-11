# Custom actions library

This page describes reusable custom-action recipes. Each can be created inside the app without importing any files.

## How to read the recipes
- Type tells you whether the action is a URL or a script.
- Target notes whether the action uses the device host or a specific override.
- Purpose describes when to use it.

## Recipes

| Name | Type | Target | Purpose | Notes |
| --- | --- | --- | --- | --- |
| Admin Console | URL | Device host | Open the primary admin UI for the device. | Use the HTTPS port if the service is web-based. |
| Metrics Dashboard | URL | Host override | Open a metrics or monitoring UI. | Point to a metrics host if it is separate from the device. |
| Logs Viewer | URL | Device host | Open a web UI that lists logs. | Pair with a read-only account if available. |
| Restart Service | Script | Device host | Restart a single service after a deploy. | Keep the command scoped to one service. |
| Reload Config | Script | Device host | Reload service configuration without downtime. | Use a reload command instead of restart if supported. |
| Health Check | Script | Device host | Run a quick status check and return output. | Useful before opening the terminal. |
| Support Page | URL | Host override | Open vendor support or status pages. | Use a public link not tied to credentials. |

## Naming guidance
- Start with the outcome, not the command.
- Keep names short and action-oriented.
- Use consistent verbs across a device group.
