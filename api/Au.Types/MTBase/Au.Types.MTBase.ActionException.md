# Property `Au.Types.MTBase.ActionException`

Whether to handle exceptions in item action code. If `false` (default), handles exceptions and on exception calls `Au.print.warning`. This property is applied to items added afterwards; submenus inherit it.

```
public bool ActionException { get; set; }
```

##### Property Value

`bool`

Default: `Au.toolbar` `false`, `Au.popupMenu` `false`.