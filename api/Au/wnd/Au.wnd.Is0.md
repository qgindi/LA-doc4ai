# Property `Au.wnd.Is0`

Returns `true` if the window handle is 0 (this variable == `default(wnd)`).

```csharp
public bool Is0 { get; }
```

##### Property Value

`bool`

#### Examples

```csharp
wnd w = wnd.find("Window*");
if(w.Is0) { print.it("window not found"); return; }
```

### See Also

`Au.wnd.IsAlive`