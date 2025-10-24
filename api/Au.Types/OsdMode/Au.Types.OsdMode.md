# Enum `Au.Types.OsdMode`

Whether `Au.osdText.Show` waits or shows the OSD window in this or new thread.

```
public enum OsdMode
```

##### Remarks

If this thread has windows, any value can be used, but usually `Auto` (default) or `ThisThread` is the best.

### Fields

| Name | Description |
| --- | --- |
| Auto | Depends on `Au.process.thisThreadHasMessageLoop`. If it is `true`, uses `ThisThread`, else `StrongThread`. Does not wait. |
| StrongThread | Show the OSD window in new thread and don't wait. Set `System.Threading.Thread.IsBackground`=`false`, so that the OSD is not closed when other threads of this app end. |
| ThisThread | Show the OSD window in this thread and don't wait. This thread must must be a UI thread (with windows etc). |
| Wait | Show the OSD window in this thread and wait until it disappears. Waits `Au.osdText.SecondsTimeout` seconds. While waiting, dispatches messages etc; see `Au.wait.doEvents`. |
| WeakThread | Show the OSD window in new thread and don't wait. Set `System.Threading.Thread.IsBackground`=`true`, so that the OSD is closed when other threads of this app end. |