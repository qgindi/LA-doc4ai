# Method `Au.More.ExplorerFolder.GetSelectedItems`

Gets paths of selected items.

```
public string[] GetSelectedItems()
```

##### Returns

`string[]`

Array containing 0 or more items.

#### Remarks

For non-file-system items gets `":: ITEMIDLIST"`; see `Au.Types.Pidl`.