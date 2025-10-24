# Method `Au.Triggers.WindowTriggerArgs.ShowToolbarWhenWindowName`

## Overload 1

Shows or hides a window-attached toolbar depending on window name. Use in window trigger action, like in examples.

```
public void ShowToolbarWhenWindowName(Func<WindowTriggerArgs, toolbar> tbFunc, string windowName)
```

##### Parameters

- *tbFunc*  (`Func<Au.Triggers.WindowTriggerArgs, Au.toolbar>`):
    Toolbar function. Let it create a window-attached toolbar and returns the `Au.toolbar` object.
- *windowName*  (`string`):
    Window name when the toolbar should be visible. String format: [wildcard expression](../articles/Wildcard%20expression.html).

##### Exceptions

- `ArgumentException`:
    Invalid wildcard expression (`"**options "` or regular expression).

#### Remarks

The trigger must have argument `, later: TWLater.Name` (see `Au.Triggers.TWLater`) and match the window with any name.

#### Examples

Show toolbar `Toolbar_Chrome1` on a Chrome window when window name starts with `"NuGet"`.

```
Triggers.Window[TWEvent.ActiveOnce, "*Google Chrome", "Chrome_WidgetWin_1", later: TWLater.Name] =
	ta => ta.ShowToolbarWhenWindowName(Toolbar_Chrome1, "NuGet*");
```

Toolbar `Toolbar_Chrome1` for the above example.

```
toolbar Toolbar_Chrome1(WindowTriggerArgs ta) { var t = new toolbar(); /* add buttons */ t.Show(ta); return t; }
```

Show Toolbar_A when window name starts with `"A -"`, Toolbar_B when `"B -"`, and Toolbar_C always.

```
Triggers.Window[TWEvent.ActiveOnce, "*Google Chrome", "Chrome_WidgetWin_1", later: TWLater.Name] = ta => {
	ta.ShowToolbarWhenWindowName(Toolbar_A, "A -*");
	ta.ShowToolbarWhenWindowName(Toolbar_B, "B -*");
	if (ta.Later == 0) Toolbar_C(ta);
};
```

* * *

## Overload 2

Shows or hides a window-attached toolbar depending on window name. Use in window trigger action, like in examples.

```
public void ShowToolbarWhenWindowName(Func<WindowTriggerArgs, toolbar> tbFunc, Func<wnd, bool> windowName)
```

##### Parameters

- *tbFunc*  (`Func<Au.Triggers.WindowTriggerArgs, Au.toolbar>`):
    Toolbar function. Let it create a window-attached toolbar and returns the `Au.toolbar` object.
- *windowName*  (`Func<Au.wnd, bool>`):
    Callback function that returns `true` if the toolbar should be visible.

#### Examples

Show toolbar `Toolbar_Chrome2` on a Chrome window when web page URL starts with `"https://www.youtube.com/"`.

```
Triggers.Window[TWEvent.ActiveOnce, "*Google Chrome", "Chrome_WidgetWin_1", later: TWLater.Name] = ta => ta.ShowToolbarWhenWindowName(Toolbar_Chrome2, w => {
	var e = w.Elm["web:DOCUMENT"].Find(-1);
	return e != null && e.Value.Starts("https://www.youtube.com/");
});
```