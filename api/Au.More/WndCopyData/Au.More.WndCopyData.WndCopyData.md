# Constructor of `Au.More.WndCopyData`

Initializes this variable from *lParam* of a received `WM_COPYDATA` message. Then you can call functions of this variable to get data in managed format.

```
public WndCopyData(nint lParam)
```

##### Parameters

- *lParam*  (`nint`):
    *lParam* of a `WM_COPYDATA` message received in a window procedure. It is `COPYDATASTRUCT` pointer.