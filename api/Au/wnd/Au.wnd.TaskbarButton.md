# Property `Au.wnd.TaskbarButton`

Returns an object that manages the taskbar button of this window: flash, progress, add/delete.

```
public WTaskbarButton TaskbarButton { get; }
```

##### Property Value

`Au.Types.WTaskbarButton`

#### Examples

```
var w = wnd.find(0, "*Notepad", "Notepad");
w.TaskbarButton.Delete();
```