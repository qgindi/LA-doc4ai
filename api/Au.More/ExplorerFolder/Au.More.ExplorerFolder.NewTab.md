# Method `Au.More.ExplorerFolder.NewTab`

Adds new tab in a folder window.

```csharp
public static ExplorerFolder NewTab(wnd w, string folder = null)
```

##### Parameters

- *w*  (`Au.wnd`):
  A folder window.
- *folder*  (`string`):
  If not `null`, calls `Au.More.ExplorerFolder.Open`.

##### Returns

`Au.More.ExplorerFolder`

`Au.More.ExplorerFolder` of the new tab.

##### Exceptions

- `Exception`:
  Failed.

#### Remarks

This method may stop working after a windows update. Because there is no Windows API, it uses undocumented UI element names (they may change).