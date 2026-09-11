# Property `Au.wnd.getwnd.LastChild`

Gets the last direct child control in the Z order.

```csharp
public wnd LastChild { get; }
```

##### Property Value

`Au.wnd`

`default(wnd)` if no children or if failed.

#### Remarks

Calls API `GetWindow`.
Supports`Au.lastError`.