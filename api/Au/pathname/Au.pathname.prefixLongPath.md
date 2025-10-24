# Method `Au.pathname.prefixLongPath`

If *path* is full path (see `Au.pathname.isFullPath`) and does not start with `@"\\?\"`, prepends `@"\\?\"`. If *path* is network path (like `@"\\computer\folder\..."`), makes like `@"\\?\UNC\computer\folder\..."`.

```
public static string prefixLongPath(string path)
```

##### Parameters

- *path*  (`string`):
    Path. Can be `null`. Must not start with `"%environmentVariable%"`. This function does not expand it. See `Au.pathname.expand`.

##### Returns

`string`

#### Remarks

Windows API kernel functions support extended-length paths, ie longer than 259 characters. But the path must have this prefix. Windows API shell functions don't support it.