# Class `Au.trayIcon`

Shows tray icon.

```
public class trayIcon : IDisposable
```

##### Remarks

Wraps API `Shell_NotifyIconW`, `NOTIFYICONDATAW`. More info there.

This thread must dispatch messages.

Can be used by multiple threads (eg one thread adds tray icon and other thread later changes its tooltip).

Creates a hidden window that receives tray icon events (click etc).

##### Inheritance

`object` → `trayIcon`

### Constructors

`trayIcon(int, bool)`

### Fields

`MsgNotify`

### Properties

`Hwnd`, `Icon`, `Id`, `Tooltip`, `Visible`, `notificationIconSize`

### Methods

`Dispose`, `Dispose`, `Focus`, `GetRect`, `HideNotification`, `ShowNotification`, `WndProc`

### Events

`Click`, `Message`, `MiddleClick`, `NotificationClick`, `PopupClose`, `PopupOpen`, `RightClick`