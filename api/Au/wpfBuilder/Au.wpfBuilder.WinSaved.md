# Method `Au.wpfBuilder.WinSaved`

Saves window xy/size/state when closing and restores when opening.

```
public wpfBuilder WinSaved(string saved, Action<string> save)
```

##### Parameters

- *saved*  (`string`):
    String that the *save* action received previously. Can be `null` or `""`, usually first time (still not saved).
- *save*  (`Action<string>`):
    Called when closing the window. Receives string containing window xy/size/state. Can save it in registry, file, anywhere.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:

    - Container is not of type `Window`.
    - Cannot be after `Au.wpfBuilder.WinXY`, `Au.wpfBuilder.WinRect` or `Au.wpfBuilder.WinSaved(string, Action<string>)`.
    - Window is loaded.

#### Remarks

Calls `Au.More.WndSavedRect.Restore`. Call this function before showing the window. Don't change location/size-related window properties after that. If you use `Au.wpfBuilder.WinSize`, call it before. It is used if size is still not saved. The same if you set window position or state.

#### Examples

```
string rk = @"HKEY_CURRENT_USER\Software\Au\Test", rv = "winSR";
var b = new wpfBuilder("Window").WinSize(300);
b.Row(0).Add("Text", out TextBox _);
b.R.AddOkCancel();
b.WinSaved(Microsoft.Win32.Registry.GetValue(rk, rv, null) as string, o => Microsoft.Win32.Registry.SetValue(rk, rv, o));
b.End();
```