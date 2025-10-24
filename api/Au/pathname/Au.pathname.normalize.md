# Method `Au.pathname.normalize`

Makes normal full path from path that can contain special substrings etc.

```
public static string normalize(string path, string defaultParentDirectory = null, PNFlags flags = 0)
```

##### Parameters

- *path*  (`string`):
    Any path.
- *defaultParentDirectory*  (`string`):
    If *path* is not full path, combine it with *defaultParentDirectory* to make full path.
- *flags*  (`Au.Types.PNFlags`)

##### Returns

`string`

##### Exceptions

- `ArgumentException`:
    *path* is not full path, and *defaultParentDirectory* is not used or does not make it full path.

#### Remarks

The sequence of actions:

1. If *path* starts with `'%'` character, expands environment variables and special folder names. See `Au.pathname.expand`.
2. If *path* is not full path but looks like URL, and used flag `CanBeUrl`, returns *path*.
3. If *path* is not full path, and *defaultParentDirectory* is not `null`/`""`, combines *path* with `expand(defaultParentDirectory)`.
4. If *path* is not full path, throws exception.
5. If *path* is like `"C:"` makes like `"C:\"`.
6. Calls API `GetFullPathName`. It replaces `'/'` with `'\\'`, replaces multiple `'\\'` with single (where need), processes `@"\.."` etc, trims spaces, etc.
7. If no flag `DontExpandDosPath`, if *path* looks like a short DOS path version (contains `'~'` etc), calls API `GetLongPathName`. It converts short DOS path to normal path, if possible, for example `@"c:\progra~1"` to `@"c:\program files"`. It is slow. It converts path only if the file exists.
8. If no flag `DontRemoveEndSeparator`, and string ends with `'\\'` character, and length > 4, removes the `'\\'`, unless then it would be a path to an existing file (not directory).
9. If no flag `DontPrefixLongPath`, calls `Au.pathname.prefixLongPathIfNeed`, which adds `@"\\?\"` etc prefix if path is very long.

Similar to `System.IO.Path.GetFullPath`. Main differences: this function expands environment variables, does not support relative paths (unless used *defaultParentDirectory*), trims `'\\'` at the end if need.

### See Also

`Au.filesystem.more.getFinalPath`