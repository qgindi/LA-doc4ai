# Method `Au.More.WndCopyData.Send`

Sends string or other data to a window of any process. Uses API `SendMessage` `WM_COPYDATA`.

```
public static nint Send<T>(wnd w, int dataId, ReadOnlySpan<T> data, nint wParam = 0) where T : unmanaged
```

##### Parameters

- *w*  (`Au.wnd`):
    The window.
- *dataId*  (`int`):
    Data id. It is `COPYDATASTRUCT.dwData`.
- *data*  (`ReadOnlySpan<T>`):
    Data. For example string or `byte[]`. String can contain `'\0'` characters.
- *wParam*  (`nint`):
    Can be any value. Optional.

##### Returns

`nint`

`SendMessage`'s return value.

##### Type Parameters

- `T`:
    Type of data elements. For example, `char` for string, `byte` for `byte[]`.