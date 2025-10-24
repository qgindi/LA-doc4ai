# Method `Au.More.WndUtil.GetWindowsStoreAppId`

Gets window Windows Store app user model id, like `"Microsoft.WindowsCalculator_8wekyb3d8bbwe!App"`.

```
public static string GetWindowsStoreAppId(wnd w, bool prependShellAppsFolder = false, bool getExePathIfNotWinStoreApp = false)
```

##### Parameters

- *w*  (`Au.wnd`):
    A top-level window.
- *prependShellAppsFolder*  (`bool`):
    Prepend `@"shell:AppsFolder\"` (to run or get icon).
- *getExePathIfNotWinStoreApp*  (`bool`):
    Get program path if it is not a Windows Store app.

##### Returns

`string`

`null` if failed. On Windows 7 returns `null` unless *getExePathIfNotWinStoreApp* `true`.

#### Remarks

Most Windows Store app windows have class name `"Windows.UI.Core.CoreWindow"` or `"ApplicationFrameWindow"`.