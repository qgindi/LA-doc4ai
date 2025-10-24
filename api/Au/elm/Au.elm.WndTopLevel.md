# Property `Au.elm.WndTopLevel`

Gets the top-level window that contains this UI element.

```
public wnd WndTopLevel { get; }
```

##### Property Value

`Au.wnd`

`default(wnd)` if failed. Supports `Au.lastError`.

#### Remarks

All UI elements must support this property, but some have bugs and can return `default(wnd)`. Uses API `WindowFromAccessibleObject` and API `GetAncestor`.