# Method `Au.More.ExplorerFolder.Of`

Creates `Au.More.ExplorerFolder` for a folder window.

```
public static ExplorerFolder Of(wnd w, string tab = null)
```

##### Parameters

- *w*  (`Au.wnd`):
    A folder window.
- *tab*  (`string`):
    Tab name (wildcard expression). If null (default), uses the current tab.

##### Returns

`Au.More.ExplorerFolder`

`null` if failed.

##### Exceptions

- `Au.Types.AuWndException`:
    *w* invalid.