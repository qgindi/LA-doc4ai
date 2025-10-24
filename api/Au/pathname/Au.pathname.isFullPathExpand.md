# Method `Au.pathname.isFullPathExpand`

## Overload 1

Expands environment variables and calls/returns `Au.pathname.isFullPath`.

```
public static bool isFullPathExpand(ref string path, bool? strict = null)
```

##### Parameters

- *path*  (`string`):
    Any string. Can be `null`. If starts with `'%'` character, calls `Au.pathname.expand` and then `Au.pathname.isFullPath` with expanded environment variables. If it returns `true`, replaces the passed variable with the expanded path string.
- *strict*  (`bool?`):

    What to do if *path* looks like starts with and environment variable or known folder but the variable/folder does not exist:

    - `true` - throw `System.ArgumentException`;
    - `false` - return unexpanded path;
    - `null` (default) - call `Au.print.warning` and return unexpanded path.

##### Returns

`bool`

`true` if the string is full path, like `@"C:\a\b.txt"` or `@"C:"` or `@"\\server\share\..."`.

#### Remarks

Returns `true` if *path* matches one of these wildcard patterns:

- `@"?:\*"` - local path, like `@"C:\a\b.txt"`. Here `?` is A-Z, a-z.
- `@"?:"` - drive name, like `@"C:"`. Here `?` is A-Z, a-z.
- `@"\\*"` - network path, like `@"\\server\share\..."`. Or has prefix `@"\\?\"`.

Supports `'/'` characters too. Supports only file-system paths. Returns `false` if *path* is URL (`Au.pathname.isUrl`) or starts with `"::"`.

* * *

## Overload 2

Expands environment variables and calls/returns `Au.pathname.isFullPath`.

```
public static bool isFullPathExpand(string path, out string path2, bool? strict = null)
```

##### Parameters

- *path*  (`string`):
    Any string. Can be `null`. If starts with `'%'` character, calls `Au.pathname.expand` and then `Au.pathname.isFullPath` with expanded environment variables. If it returns `true`, sets *path2* = the expanded path string.
- *path2*  (`string`):
    Receives the final path.
- *strict*  (`bool?`):

    What to do if *path* looks like starts with and environment variable or known folder but the variable/folder does not exist:

    - `true` - throw `System.ArgumentException`;
    - `false` - return unexpanded path;
    - `null` (default) - call `Au.print.warning` and return unexpanded path.

##### Returns

`bool`

`true` if the string is full path, like `@"C:\a\b.txt"` or `@"C:"` or `@"\\server\share\..."`.

#### Remarks

Returns `true` if *path* matches one of these wildcard patterns:

- `@"?:\*"` - local path, like `@"C:\a\b.txt"`. Here `?` is A-Z, a-z.
- `@"?:"` - drive name, like `@"C:"`. Here `?` is A-Z, a-z.
- `@"\\*"` - network path, like `@"\\server\share\..."`. Or has prefix `@"\\?\"`.

Supports `'/'` characters too. Supports only file-system paths. Returns `false` if *path* is URL (`Au.pathname.isUrl`) or starts with `"::"`.