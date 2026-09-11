# Method `Au.filesystem.more.notifyShell`

Calls API `SHChangeNotify`.

```csharp
public static void notifyShell(SCNEvent eventId, string path, string path2 = null, SCNFlags flags = 0)
```

##### Parameters

- *eventId*  (`Au.Types.SCNEvent`):
  Parameter *wEventId* of `SHChangeNotify`.
- *path*  (`string`):
  Parameter *dwItem1* of `SHChangeNotify`. File/folder path or `null`, depending on *eventId*.
- *path2*  (`string`):
  Parameter *dwItem2* of `SHChangeNotify`.
- *flags*  (`Au.Types.SCNFlags`):
  Parameter *uFlags* of `SHChangeNotify`. This method adds `SHCNF_PATH`.

#### Remarks

Can be used to notify shell (File Explorer folder windows, desktop, etc) about a filesystem change in case it does not update something automatically. Or to update faster (use a flush flag).