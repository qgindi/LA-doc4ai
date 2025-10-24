# Method `Au.More.FileSystemRedirection.IsSystem64PathIn32BitProcess`

Returns `true` if `Au.osVersion.is32BitProcessAnd64BitOS` is `true` and path starts with `Au.folders.System`. Most such paths are redirected, therefore you may want to disable redirection with this class.

```
public static bool IsSystem64PathIn32BitProcess(string path)
```

##### Parameters

- *path*  (`string`):
    Normalized path. This function does not normalize. Also it is unaware of `@"\\?\"`.

##### Returns

`bool`