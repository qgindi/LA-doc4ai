# Method `Au.filesystem.setAttributes`

Sets file or directory attributes.

```
public static bool setAttributes(string path, FileAttributes attributes, bool? add = null, FAFlags flags = 0)
```

##### Parameters

- *path*  (`string`):
    Full path. Supports `@"\.."` etc. If flag `UseRawPath` not used, supports environment variables (see `Au.pathname.expand`).
- *attributes*  (`FileAttributes`):
    Attributes to set, add or remove.
- *add*  (`bool?`):
    `null` (default) - set; `true` - add; `false` - remove.
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

Calls API `SetFileAttributes`. For NTFS links, sets attributes of the link, not of its target.