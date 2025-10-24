# Method `Au.script.trayIcon`

Adds standard tray icon.

```
public static void trayIcon(int delay = 500, Action<trayIcon> init = null, Action<trayIcon, popupMenu> menu = null, string f_ = null)
```

##### Parameters

- *delay*  (`int`):
    Delay, milliseconds.
- *init*  (`Action<Au.trayIcon>`):
    Called before showing the tray icon. Can set its properties and event handlers.
- *menu*  (`Action<Au.trayIcon, Au.popupMenu>`):
    Called before showing context menu. Can add menu items. Menu item actions must not block messages etc for long time; if need, run in other thread or process (`Au.script.run`).
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html). Don't use. Or set = `null` to disable script editing via the tray icon.

#### Remarks

Uses other thread. The *init* and *menu* actions run in that thread too. It dispatches messages, therefore they also can set timers (`Au.timer`), create hidden windows, etc. Current thread does not have to dispatch messages.

Does nothing if role `editorExtension`.

#### Examples

How to change icon and tooltip.

```
script.trayIcon(init: t => { t.Icon = icon.stock(StockIcon.HELP); t.Tooltip = "Example"; });
```

How to add menu items.

```
script.trayIcon(menu: (t, m) => {
	m["Example"] = o => { dialog.show("Example"); };
	m["Run another script"] = o => { script.run("Example.cs"); };
});
```

### See Also

`Au.trayIcon`