# Method `Au.Types.Pidl.FromString`

Converts string to `ITEMIDLIST` and creates new `Au.Types.Pidl` variable that holds it.

```
public static Pidl FromString(string s, bool throwIfFailed = false)
```

##### Parameters

- *s*  (`string`):
    A file-system path or URL or shell object parsing name (see `Au.Types.Pidl.ToShellString`) or `":: ITEMIDLIST"` (see `Au.Types.Pidl.ToHexString`). Supports environment variables (see `Au.pathname.expand`).
- *throwIfFailed*  (`bool`):
    Throw exception if failed.

##### Returns

`Au.Types.Pidl`

`null` if failed.

##### Exceptions

- `Au.Types.AuException`:
    Failed, and *throwIfFailed* is `true`. Probably invalid *s*.

#### Remarks

Calls `SHParseDisplayName`, except when string is `":: ITEMIDLIST"`. If `":: ITEMIDLIST"`, does not check whether the shell object exists.