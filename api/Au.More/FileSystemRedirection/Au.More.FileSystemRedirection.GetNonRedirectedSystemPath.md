# Method `Au.More.FileSystemRedirection.GetNonRedirectedSystemPath`

If `Au.osVersion.is32BitProcessAnd64BitOS` is `true` and *path* starts with `Au.folders.System`, replaces that path part with `Au.folders.SystemX64`. It disables redirection to `Au.folders.SystemX86` for that path.

```
public static string GetNonRedirectedSystemPath(string path, bool ifExistsOnlyThere = false)
```

##### Parameters

- *path*  (`string`):
    Normalized path. This function does not normalize. Also it is unaware of `@"\\?\"`.
- *ifExistsOnlyThere*  (`bool`):
    Don't replace *path* if the file or directory exists in the redirected folder or does not exist in the non-redirected folder.

##### Returns

`string`