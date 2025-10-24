# Method `Au.pathname.prefixLongPathIfNeed`

Calls `Au.pathname.prefixLongPath` if *path* is longer than `Au.pathname.maxDirectoryPathLength` (247).

```
public static string prefixLongPathIfNeed(string path)
```

##### Parameters

- *path*  (`string`):
    Path. Can be `null`. Must not start with `"%environmentVariable%"`. This function does not expand it. See `Au.pathname.expand`.

##### Returns

`string`