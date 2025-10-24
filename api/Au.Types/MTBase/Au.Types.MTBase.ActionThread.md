# Property `Au.Types.MTBase.ActionThread`

Execute item actions asynchronously in new threads. This property is applied to items added afterwards; submenus inherit it.

```
public bool ActionThread { get; set; }
```

##### Property Value

`bool`

Default: `Au.toolbar` `true`, `Au.popupMenu` `false`.

#### Remarks

If current thread is a UI thread (has windows etc) or has triggers or hooks, and item action functions execute some long automations etc in current thread, current thread probably is hung during that time. Set this property = `true` to avoid it.