# Method `Au.More.ExplorerFolder.All`

Creates `Au.More.ExplorerFolder` for all folder windows.

```
public static ExplorerFolder[] All(bool onlyFilesystem = false, wnd tabsOf = default)
```

##### Parameters

- *onlyFilesystem*  (`bool`):
    Skip folders that don't have a filesystem path, such as Control Panel and Recycle Bin.
- *tabsOf*  (`Au.wnd`):
    Need only tabs of this window.

##### Returns

`Au.More.ExplorerFolder[]`