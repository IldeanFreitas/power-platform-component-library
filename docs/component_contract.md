# cmpAppHeader contract

## Purpose

Provide a configurable application header without reading a datasource,
navigating directly, or depending on a tenant-specific asset.

## Inputs

| Property | Type | Default | Purpose |
|---|---|---|---|
| `AppName` | Text | `"Sample Workspace"` | Visible application name. |
| `UserDisplayName` | Text | `""` | Optional greeting target. |
| `AccentColor` | Color | Blue | Product accent supplied by the parent app. |
| `Theme` | Text | `"light"` | `light` or `dark`; unexpected values fall back to light. |
| `Variant` | Text | `"default"` | `compact`, `default`, or `prominent`. |
| `ShowNotifications` | Boolean | `true` | Toggles the notification action. |
| `NotificationCount` | Number | `0` | Shows a badge when greater than zero. |

## Events

| Event | Owner | Reason |
|---|---|---|
| `OnBrandSelect` | Parent app | The component must not decide the destination screen. |
| `OnNotificationSelect` | Parent app | The consuming app owns notification state and navigation. |
| `OnProfileSelect` | Parent app | The consuming app owns profile/menu behavior. |

## Responsive behavior

- The component fills the width of its parent container.
- At widths below 480px, the greeting is hidden to preserve primary actions.
- The `compact` variant is intended for constrained layouts.
- Action buttons maintain a minimum 44px target in the reference design.

## Boundaries

- No SharePoint, Dataverse, Office 365, API, or connector reference.
- No `Navigate`, `Patch`, `Collect`, or global-state mutation inside the component.
- No customer logo, user photo, environment identifier, or application-specific copy.
