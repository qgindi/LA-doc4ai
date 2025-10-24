# Method `Au.wnd.ClassNameIs`

## Overload 1

Returns `true` if the class name of this window matches *cn*. Else returns `false`. Also returns `false` when fails (probably window closed or 0 handle). Supports `Au.lastError`.

```
public bool ClassNameIs(string cn)
```

##### Parameters

- *cn*  (`string`):
    Class name. Case-insensitive wildcard. See `Au.Types.ExtString.Like`. Cannot be `null`.

##### Returns

`bool`

### See Also

`Au.wnd.IsMatch`

* * *

## Overload 2

If window class name matches one of strings in *classNames*, returns 1-based string index. Else returns 0. Also returns 0 if fails to get class name (probably window closed or 0 handle). Supports `Au.lastError`.

```
public int ClassNameIs(params ReadOnlySpan<string> classNames)
```

##### Parameters

- *classNames*  (`ReadOnlySpan<string>`):
    Class names. Case-insensitive wildcard. See `Au.Types.ExtString.Like`. The array and strings cannot be `null`.

##### Returns

`int`