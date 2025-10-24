# Constructor of `Au.More.WinformsControlNames`

Prepares to get control names.

```
public WinformsControlNames(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`):
    Any top-level or child window of that process.

##### Exceptions

- `Au.Types.AuWndException`:
    *w* invalid.
- `Au.Types.AuException`:
    Failed to allocate process memory (see `Au.More.ProcessMemory`) needed to get control names, usually because of [UAC](../articles/UAC.html).