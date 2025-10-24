# Method `Au.wnd.GetClientRect`

Gets client area rectangle.

```
public bool GetClientRect(out RECT r, bool inScreen = false)
```

##### Parameters

- *r*  (`Au.Types.RECT`):
    Receives the rectangle. Will be `default(RECT)` if failed.
- *inScreen*  (`bool`):
    Get rectangle in screen coordinates; like `Au.wnd.GetWindowAndClientRectInScreen` but faster. If `false` (default), calls API `GetClientRect`; the same as `Au.wnd.ClientRect`.

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.