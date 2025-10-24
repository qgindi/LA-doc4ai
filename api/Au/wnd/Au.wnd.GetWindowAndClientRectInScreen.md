# Method `Au.wnd.GetWindowAndClientRectInScreen`

Gets window rectangle and client area rectangle, both in screen coordinates.

```
public bool GetWindowAndClientRectInScreen(out RECT rWindow, out RECT rClient)
```

##### Parameters

- *rWindow*  (`Au.Types.RECT`):
    Receives window rectangle.
- *rClient*  (`Au.Types.RECT`):
    Receives client area rectangle.

##### Returns

`bool`

#### Remarks

Calls API `GetWindowInfo`. Supports `Au.lastError`.