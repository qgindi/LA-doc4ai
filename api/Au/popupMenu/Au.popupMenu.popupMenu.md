# Constructor of `Au.popupMenu`

## Overload 1

Use this constructor for various context menus of your app.

```csharp
public popupMenu()
```

#### Remarks

Users cannot right-click a menu item and open/select it in editor.

* * *

## Overload 2

Use this constructor in scripts.

```csharp
public popupMenu(string name, string f_ = null, int l_ = 0)
```

##### Parameters

- *name*  (`string`):
  Menu name. Must be a unique valid filename. Currently not used. Can be `null`.
- *f_*  (`string`):
  [Caller info parameter](🔗)
- *l_*  (`int`):
  [Caller info parameter](🔗)

#### Remarks

This overload sets `Au.Types.MTBase.ExtractIconPathFromCode` = `true`.

Users can right-click an item to open/select it in editor, unless *f_* is explicitly set = `null`.