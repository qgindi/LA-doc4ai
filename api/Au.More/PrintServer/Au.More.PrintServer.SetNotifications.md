# Method `Au.More.PrintServer.SetNotifications`

Sets window/message to be notified about server events.

```
public void SetNotifications(wnd w, int message)
```

##### Parameters

- *w*  (`Au.wnd`):
    Your window that displays output, or any other window. Its window procedure on *message* should call `Au.More.PrintServer.GetMessage` until it returns `false`. See example in class help.
- *message*  (`int`):
    Windows message to send to *w* when one or more output events are available. For example `WM_USER` or `WM_APP`.