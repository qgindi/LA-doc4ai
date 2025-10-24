# Method `Au.More.FileSystemRedirection.Disable`

If `Au.osVersion.is32BitProcessAnd64BitOS`, calls API `Wow64DisableWow64FsRedirection`, which disables file system redirection.

```
public void Disable()
```

#### Remarks

The caller can call this without checking OS and process bitness. This function checks it and it is fast.

Always call `Au.More.FileSystemRedirection.Revert` or `Au.More.FileSystemRedirection.Dispose`, for example use `finally` or `using` statement. Not calling it is more dangerous than a memory leak. It is not called by GC.