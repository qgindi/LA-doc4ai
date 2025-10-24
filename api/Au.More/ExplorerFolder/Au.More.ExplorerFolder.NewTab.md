# Method `Au.More.ExplorerFolder.NewTab`

Adds new tab in a folder window.

```
public static ExplorerFolder NewTab(wnd w, string folder = null)
```

##### Parameters

- *w*  (`Au.wnd`):
    A folder window.
- *folder*  (`string`):
    If not null, calls `Au.More.ExplorerFolder.Open`.

##### Returns

`Au.More.ExplorerFolder`

`Au.More.ExplorerFolder` for the new tab.

##### Exceptions

- `Exception`:
    Failed.

#### Remarks

To create new tab, activates the window and sends keys `Ctrl+T`.