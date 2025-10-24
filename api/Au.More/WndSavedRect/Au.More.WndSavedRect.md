# Struct `Au.More.WndSavedRect`

Helps to save and restore window rectangle and state. Ensures in screen, per-monitor-DPI-aware, etc.

```
public struct WndSavedRect
```

##### Examples

WPF window created with `Au.wpfBuilder`.

```
const string c_rkey = @"HKEY_CURRENT_USER\Software\Au\Test", c_rvalue = @"Wpf7.Rect";
var b = new wpfBuilder("Window").WinSize(400).R.AddOkCancel().End();
	
WndSavedRect.Restore(b.Window, Registry.GetValue(c_rkey, c_rvalue, null) as string, s1 => Registry.SetValue(c_rkey, c_rvalue, s1));

//the same
//b.WinSaved(Registry.GetValue(c_rkey, c_rvalue, null) as string, s1 => Registry.SetValue(c_rkey, c_rvalue, s1));

if (!b.ShowDialog()) return;
```

### Constructors

`WndSavedRect(wnd)`, `WndSavedRect(Form)`, `WndSavedRect(Window)`

### Properties

`Dpi`, `IsToolWindow`, `Maximize`, `RawRect`

### Methods

`FromString`, `NormalizeRect`, `Restore`, `Restore`, `ToString`