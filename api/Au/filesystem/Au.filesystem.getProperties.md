# Method `Au.filesystem.getProperties`

Gets file or directory attributes, size and times.

```
public static bool getProperties(string path, out FileProperties properties, FAFlags flags = 0)
```

##### Parameters

- *path*  (`string`):
    Full path. Supports `@"\.."` etc. If flag `UseRawPath` not used, supports environment variables (see `Au.pathname.expand`).
- *properties*  (`Au.Types.FileProperties`):
    Receives properties.
- *flags*  (`Au.Types.FAFlags`)

##### Returns

`bool`

`false` if the file/directory does not exist.

##### Exceptions

- `ArgumentException`:
    Not full path (when not used flag `UseRawPath`).
- `Au.Types.AuException`:
    The file/directory exists but failed to get its properties. Not thrown if used flag `DontThrow`.

#### Remarks

Calls API `GetFileAttributesEx`. Supports `Au.lastError` (useful with flag `DontThrow`). For NTFS links, gets properties of the link, not of its target. You can also get most of these properties with `Au.filesystem.enumerate`.