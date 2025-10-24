# Method `Au.pathname.unprefixLongPath`

If *path* starts with `@"\\?\"` prefix, removes it. If *path* starts with `@"\\?\UNC\"` prefix, removes `@"?\UNC\"`.

```
public static string unprefixLongPath(string path)
```

##### Parameters

- *path*  (`string`):
    Path. Can be `null`. Must not start with `"%environmentVariable%"`. This function does not expand it. See `Au.pathname.expand`.

##### Returns

`string`