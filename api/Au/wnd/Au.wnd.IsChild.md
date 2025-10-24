# Property `Au.wnd.IsChild`

Returns `true` if this is a child window (control), `false` if top-level window.

```
public bool IsChild { get; }
```

##### Property Value

`bool`

#### Remarks

Supports `Au.lastError`. Another way is `w.HasStyle(WS.CHILD)`. It is faster but less reliable, because some top-level windows have `WS_CHILD` style and some child windows don't.

### See Also

`Au.wnd.getwnd.DirectParent`