# Usage examples

## Minimal header

```powerfx
cmpAppHeader.AppName = "Operations Hub"
```
## Header with parent-owned events

```powerfx
cmpAppHeader.AppName = "Service Desk"
cmpAppHeader.UserDisplayName = varCurrentUserName
cmpAppHeader.NotificationCount = CountRows(colOpenAlerts)
cmpAppHeader.OnBrandSelect = Navigate(scrHome)
cmpAppHeader.OnNotificationSelect = Set(varShowAlerts, true)
cmpAppHeader.OnProfileSelect = Set(varShowProfileMenu, !varShowProfileMenu)
```

## Dark, compact layout

```powerfx
cmpAppHeader.Theme = "dark"
cmpAppHeader.Variant = "compact"
cmpAppHeader.AccentColor = ColorValue("#2563EB")
cmpAppHeader.ShowNotifications = false
```
