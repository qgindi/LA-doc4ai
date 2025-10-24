# Method `Au.More.StringUtil.GetEncoding`

## Overload 1

Calls `System.Text.Encoding.GetEncoding`, and `System.Text.Encoding.RegisterProvider` if need.

```
public static Encoding GetEncoding(string name)
```

##### Parameters

- *name*  (`string`)

##### Returns

`Encoding`

`null` if failed.

* * *

## Overload 2

Calls `System.Text.Encoding.GetEncoding`, and `System.Text.Encoding.RegisterProvider` if need.

```
public static Encoding GetEncoding(int codepage)
```

##### Parameters

- *codepage*  (`int`):
    If -1, uses the current Windows ANSI code page (API `GetACP`).

##### Returns

`Encoding`

`null` if failed.