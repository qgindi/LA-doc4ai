# Property `Au.wnd.TaskbarButton`

Returns an object that manages the taskbar button of this window: flash, progress, add/delete.

```csharp
public WTaskbarButton TaskbarButton { get; }
```

##### Property Value

`Au.Types.WTaskbarButton`

#### Examples

```csharp
var w = wnd.find(0, "*Example");
w.TaskbarButton.Delete();
```