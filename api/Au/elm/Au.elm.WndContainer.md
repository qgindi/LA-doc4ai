# Property `Au.elm.WndContainer`

Gets the container window or control of this UI element.

```
public wnd WndContainer { get; }
```

##### Property Value

`Au.wnd`

`default(wnd)` if failed. Supports `Au.lastError`.

#### Remarks

All UI elements must support this property, but some have bugs and can fail or return a wrong window. Uses API `WindowFromAccessibleObject`.