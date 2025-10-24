# Method `Au.icon.ofPidl`

Gets icon of a file or other shell object specified as `ITEMIDLIST`.

```
public static icon ofPidl(Pidl pidl, int size = 16)
```

##### Parameters

- *pidl*  (`Au.Types.Pidl`):
    `ITEMIDLIST`.
- *size*  (`int`):
    Icon width and height. Default 16.

##### Returns

`Au.icon`

`null` if failed.