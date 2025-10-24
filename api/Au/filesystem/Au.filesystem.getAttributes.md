# Method `Au.filesystem.getAttributes`

Gets file or directory attributes.

```
public static bool getAttributes(string path, out FileAttributes attributes, FAFlags flags = 0)
```

##### Parameters

- *path*  (`string`):
    Full path. Supports `@"\.."` etc. If flag `UseRawPath` not used, supports environment variables (see `Au.pathname.expand`).
- *attributes*  (`FileAttributes`):
    Receives attributes, or 0 if failed.
- *flags*  (`Au.Types.FAFlags`)

##### Returns

`bool`

`false` if the file/directory does not exist.

##### Exceptions

- `ArgumentException`:
    Not full path (when not used flag `UseRawPath`).
- `Au.Types.AuException`:
    Failed. Not thrown if used flag `DontThrow`.

#### Remarks

Calls API `GetFileAttributes`. Supports `Au.lastError` (useful with flag `DontThrow`). For NTFS links, gets attributes of the link, not of its target.