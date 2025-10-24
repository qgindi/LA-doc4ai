# Method `Au.clipboardData.getBinary`

## Overload 1

Gets clipboard data of any format as `byte[]`.

```
public static byte[] getBinary(int format)
```

##### Parameters

- *format*  (`int`)

##### Returns

`byte[]`

`null` if there is no data of this format.

##### Exceptions

- `ArgumentException`:
    Invalid *format*. Supported are all registered formats and standard formats `<CF_MAX` except GDI handles.
- `Au.Types.AuException`:
    Failed to open clipboard (after 10 s of wait/retry).

* * *

## Overload 2

Gets clipboard data of any format without copying to array. Uses a callback function.

```
public static T getBinary<T>(int format, Func<nint, int, T> get)
```

##### Parameters

- *format*  (`int`)
- *get*  (`Func<nint, int, T>`):
    Callback function that receives data. The clipboard is open until it returns. The data is read-only.

##### Returns

`T`

The return value of the callback function. Returns `default(T)` if there is no data of this format.

##### Exceptions

- `ArgumentException`:
    Invalid *format*. Supported are all registered formats and standard formats `<CF_MAX` except GDI handles.
- `Au.Types.AuException`:
    Failed to open clipboard (after 10 s of wait/retry).

##### Type Parameters

- `T`