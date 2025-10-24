# Method `Au.wnd.ShowNotMinMax`

If maximized or minimized, makes normal (not min/max). Also unhides.

```
public void ShowNotMinMax(int how = 0)
```

##### Parameters

- *how*  (`int`):
    What API to use: 0 `ShowWindow`, 1 `SetWindowPlacement` (no animation), 2 `WM_SYSCOMMAND`.

##### Exceptions

- `Au.Types.AuWndException`:
    The API call failed. No exception if the window did not obey.