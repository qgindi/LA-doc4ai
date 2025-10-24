# Method `Au.pathname.getRootLength`

Gets the length of the drive or network folder part in *path*, like `@"C:\"`, `@"\\server\share\"`, `@"\\?\C:\"`, `@"\\?\UNC\server\share\"`, etc.

```
public static int getRootLength(ReadOnlySpan<char> path)
```

##### Parameters

- *path*  (`ReadOnlySpan<char>`):
    Full path or any string. Can be `null`. Should not be `@"%environmentVariable%\..."`.

##### Returns

`int`

#### Remarks

See `System.IO.Path.GetPathRoot`.