# Method `Au.More.WndCopyData.SendReceive`

## Overload 1

Sends string or other data to a window of any process. Uses API `SendMessage` `WM_COPYDATA`. Receives string or other data returned by that window with `Au.More.WndCopyData.Return`.

```
public static bool SendReceive<TSend, TReceive>(wnd w, int dataId, ReadOnlySpan<TSend> send, WndCopyData.ResultReader<TReceive> receive) where TSend : unmanaged where TReceive : unmanaged
```

##### Parameters

- *w*  (`Au.wnd`):
    The window.
- *dataId*  (`int`):
    Data id. It is `COPYDATASTRUCT.dwData`.
- *send*  (`ReadOnlySpan<TSend>`):
    Data to send. For example string or `byte[]`. String can contain `'\0'` characters.
- *receive*  (`Au.More.WndCopyData`.`Au.More.WndCopyData.ResultReader<TReceive>`):
    Callback function that can convert the received data to desired format.

##### Returns

`bool`

`false` if failed.

##### Type Parameters

- `TSend`:
    Type of data elements. For example, `char` for string, `byte` for `byte[]`
- `TReceive`:
    Type of received data elements. For example, `char` for string, `byte` for `byte[]`.

* * *

## Overload 2

Calls `Au.More.WndCopyData.SendReceive<TSend, TReceive>(wnd, int, ReadOnlySpan<TSend>, ResultReader<TReceive>)` and gets the received data as `byte[]`.

```
public static bool SendReceive<TSend>(wnd w, int dataId, ReadOnlySpan<TSend> send, out byte[] received) where TSend : unmanaged
```

##### Parameters

- *w*  (`Au.wnd`):
    The window.
- *dataId*  (`int`):
    Data id. It is `COPYDATASTRUCT.dwData`.
- *send*  (`ReadOnlySpan<TSend>`):
    Data to send. For example string or `byte[]`. String can contain `'\0'` characters.
- *received*  (`byte[]`):
    The received data.

##### Returns

`bool`

`false` if failed.

##### Type Parameters

- `TSend`:
    Type of data elements. For example, `char` for string, `byte` for `byte[]`

* * *

## Overload 3

Calls `Au.More.WndCopyData.SendReceive<TSend, TReceive>(wnd, int, ReadOnlySpan<TSend>, ResultReader<TReceive>)` and gets the received string.

```
public static bool SendReceive<TSend>(wnd w, int dataId, ReadOnlySpan<TSend> send, out string received) where TSend : unmanaged
```

##### Parameters

- *w*  (`Au.wnd`):
    The window.
- *dataId*  (`int`):
    Data id. It is `COPYDATASTRUCT.dwData`.
- *send*  (`ReadOnlySpan<TSend>`):
    Data to send. For example string or `byte[]`. String can contain `'\0'` characters.
- *received*  (`string`):
    The received data.

##### Returns

`bool`

`false` if failed.

##### Type Parameters

- `TSend`:
    Type of data elements. For example, `char` for string, `byte` for `byte[]`