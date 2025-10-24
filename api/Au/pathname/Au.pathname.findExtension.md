# Method `Au.pathname.findExtension`

Finds filename extension, like `".txt"`.

```
public static int findExtension(ReadOnlySpan<char> path)
```

##### Parameters

- *path*  (`ReadOnlySpan<char>`):
    Path or filename. Can be `null`.

##### Returns

`int`

Index of `'.'` character, or -1 if there is no extension.