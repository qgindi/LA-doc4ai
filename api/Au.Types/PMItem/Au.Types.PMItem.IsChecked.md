# Property `Au.Types.PMItem.IsChecked`

Gets or sets checked state.

```
public bool IsChecked { get; set; }
```

##### Exceptions

- `InvalidOperationException`:
    The `set` function throws this exception if the item isn't checkable. Use `Au.popupMenu.AddCheck` or `Au.popupMenu.AddRadio`.

##### Property Value

`bool`