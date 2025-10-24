# Method `Au.trayIcon.ShowNotification`

Shows temporary notification window by the tray icon.

```
public void ShowNotification(string title, string text, TINFlags flags = 0, icon icon = null)
```

##### Parameters

- *title*  (`string`):
    Title, max 63 characters.
- *text*  (`string`):
    Text, max 255 characters.
- *flags*  (`Au.Types.TINFlags`):
    Standard icon and other flags.
- *icon*  (`Au.icon`):
    Custom icon. Important: use icon of size returned by `Au.trayIcon.notificationIconSize`.

#### Remarks

If the tray icon isn't visible, makes it visible.

No more than one notification at a time can be displayed. If an application attempts to display a notification when one is already being displayed, the new notification is queued and displayed when the older notification goes away.

Users may choose to not show notifications, depending on various conditions. Look in Windows **Settings > System > Notifications**.