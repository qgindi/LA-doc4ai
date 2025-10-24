# Property `Au.wnd.getwnd.root`

Calls API `GetDesktopWindow`. It gets the virtual parent window of all top-level windows.

```
public static wnd root { get; }
```

##### Property Value

`Au.wnd`

#### Remarks

> **Note:**
> It is not the desktop window (see `Au.wnd.getwnd.desktop`) that displays icons and wallpaper.