# Method `Au.More.WndCopyData.Return`

## Overload 1

Returns data to `Au.More.WndCopyData.SendReceive<TSend, TReceive>`.

```
public static int Return(void* data, int length, nint wParam)
```

##### Parameters

- *data*  (`void*`)
- *length*  (`int`)
- *wParam*  (`nint`):
    *wParam* of the received `WM_COPYDATA` message. Important, pass unchanged.

##### Returns

`int`

Your window procedure must return this value.

* * *

## Overload 2

Returns string or other data to `Au.More.WndCopyData.SendReceive<TSend, TReceive>`.

```
public static int Return<T>(ReadOnlySpan<T> data, nint wParam) where T : unmanaged
```

##### Parameters

- *data*  (`ReadOnlySpan<T>`)
- *wParam*  (`nint`):
    *wParam* of the received `WM_COPYDATA` message. Important, pass unchanged.

##### Returns

`int`

Your window procedure must return this value.

##### Type Parameters

- `T`:
    Type of data elements. For example, `char` for string, `byte` for `byte[]`