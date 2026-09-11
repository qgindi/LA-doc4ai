# Method `Au.More.ExplorerFolder.Select`

Selects a single item.

```csharp
public bool Select(string item)
```

##### Parameters

- *item*  (`string`):
  Filename (like `"example.txt"`) or full path.

##### Returns

`bool`

`false` if failed.

#### Remarks

Deselects other items. Makes the item visible (scrolls if need) and focused.

#### Examples

```csharp
ExplorerFolder.Of(wnd.find(0, cn: "CabinetWClass")).Select(item);
```