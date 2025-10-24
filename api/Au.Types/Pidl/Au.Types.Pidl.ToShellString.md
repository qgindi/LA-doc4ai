# Method `Au.Types.Pidl.ToShellString`

## Overload 1

Converts the `ITEMIDLIST` to file path or URL or shell object parsing name or display name, depending on *stringType*.

```
public string ToShellString(SIGDN stringType, bool throwIfFailed = false)
```

##### Parameters

- *stringType*  (`Au.Types.SIGDN`):

    String format. API `SIGDN`. Often used:

    - `SIGDN.NORMALDISPLAY` - returns object name without path. It is best to display in UI but cannot be parsed to create `ITEMIDLIST` again.
    - `SIGDN.FILESYSPATH` - returns path if the `ITEMIDLIST` identifies a file system object (file or directory). Else returns `null`.
    - `SIGDN.URL` - if URL, returns URL. If file system object, returns its path like `"file:///C:/a/b.txt"`. Else returns `null`.
    - `SIGDN.DESKTOPABSOLUTEPARSING` - returns path (if file system object) or URL (if URL) or shell object parsing name (if virtual object eg Control Panel). Note: not all returned parsing names can actually be parsed to create `ITEMIDLIST` again, therefore usually it's better to use `Au.Types.Pidl.ToString` instead.
- *throwIfFailed*  (`bool`):
    If failed, throw `Au.Types.AuException`.

##### Returns

`string`

Returns `null` if this variable does not have an `ITEMIDLIST` (eg disposed or detached). If failed, returns `null` or throws exception.

##### Exceptions

- `Au.Types.AuException`:
    Failed, and *throwIfFailed* is `true`.

#### Remarks

Calls `SHGetNameFromIDList`.

* * *

## Overload 2

Converts an `ITEMIDLIST` to file path or URL or shell object parsing name or display name, depending on *stringType*.

```
public static string ToShellString(nint pidl, SIGDN stringType, bool throwIfFailed = false)
```

##### Parameters

- *pidl*  (`nint`)
- *stringType*  (`Au.Types.SIGDN`):

    String format. API `SIGDN`. Often used:

    - `SIGDN.NORMALDISPLAY` - returns object name without path. It is best to display in UI but cannot be parsed to create `ITEMIDLIST` again.
    - `SIGDN.FILESYSPATH` - returns path if the `ITEMIDLIST` identifies a file system object (file or directory). Else returns `null`.
    - `SIGDN.URL` - if URL, returns URL. If file system object, returns its path like `"file:///C:/a/b.txt"`. Else returns `null`.
    - `SIGDN.DESKTOPABSOLUTEPARSING` - returns path (if file system object) or URL (if URL) or shell object parsing name (if virtual object eg Control Panel). Note: not all returned parsing names can actually be parsed to create `ITEMIDLIST` again, therefore usually it's better to use `Au.Types.Pidl.ToString` instead.
- *throwIfFailed*  (`bool`):
    If failed, throw `Au.Types.AuException`.

##### Returns

`string`

Returns `null` if *pidl* is `default(IntPtr)`. If failed, returns `null` or throws exception.

##### Exceptions

- `Au.Types.AuException`:
    Failed, and *throwIfFailed* is `true`.

#### Remarks

Calls `SHGetNameFromIDList`.