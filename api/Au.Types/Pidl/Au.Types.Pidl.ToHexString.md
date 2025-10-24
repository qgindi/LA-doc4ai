# Method `Au.Types.Pidl.ToHexString`

## Overload 1

Returns string `":: ITEMIDLIST"`. Returns `null` if this variable does not have an `ITEMIDLIST` (eg disposed or detached).

```
public string ToHexString()
```

##### Returns

`string`

#### Remarks

The string can be used with some functions of this library, mostly of classes `Au.filesystem`, `Au.Types.Pidl` and `Au.icon`. Cannot be used with native and .NET functions.

* * *

## Overload 2

Returns string `":: ITEMIDLIST"`. This overload uses an `ITEMIDLIST*` that is not stored in a `Au.Types.Pidl` variable.

```
public static string ToHexString(nint pidl)
```

##### Parameters

- *pidl*  (`nint`)

##### Returns

`string`