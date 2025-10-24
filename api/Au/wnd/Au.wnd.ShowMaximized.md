# Method `Au.wnd.ShowMaximized`

If not minimized, minimizes. Also unhides.

```
public void ShowMaximized(int how = 0)
```

##### Parameters

- *how*  (`int`):
    What API to use: 0 `ShowWindow`, 1 `SetWindowPlacement` (no animation), 2 `WM_SYSCOMMAND`.

##### Exceptions

- `Au.Types.AuWndException`:
    The API call failed. No exception if the window did not obey.