# Method `Au.toolbar.Menu`

## Overload 1

Adds button with drop-down menu.

```
public TBItem Menu(string text, Action<popupMenu> menu, MTImage image = default, int l_ = 0, string f_ = null)
```

##### Parameters

- *text*  (`string`):
    Text. Or `"Text|Tooltip"`, or `"|Tooltip"`, or `"Text|"`. Separator can be `"|"` or `"\0 "` (then `"|"` isn't a separator). To always display text regardless of `Au.toolbar.DisplayText`, append `"\a"`, like `"Text\a"` or `"Text\a|Tooltip"`.
- *menu*  (`Action<Au.popupMenu>`):
    Action that adds menu items. Called whenever the button clicked.
- *image*  (`Au.Types.MTImage`):
    Image. Read here: `Au.Types.MTBase`.
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Returns

`Au.Types.TBItem`

#### Remarks

The submenu is a `Au.popupMenu` object. It inherits these properties of this toolbar: `Au.Types.MTBase.ExtractIconPathFromCode`, `Au.Types.MTBase.ActionException`, `Au.Types.MTBase.ActionThread`, `Au.Types.MTBase.PathInTooltip`.

#### Examples

```
tb.Menu("Menu", m => {
	m["M1"]=o=>print.it(o);
	m["M2"]=o=>print.it(o);
});
```

* * *

## Overload 2

Adds button with drop-down menu.

```
public TBItem Menu(string text, Func<popupMenu> menu, MTImage image = default, int l_ = 0, string f_ = null)
```

##### Parameters

- *text*  (`string`):
    Text. Or `"Text|Tooltip"`, or `"|Tooltip"`, or `"Text|"`. Separator can be `"|"` or `"\0 "` (then `"|"` isn't a separator). To always display text regardless of `Au.toolbar.DisplayText`, append `"\a"`, like `"Text\a"` or `"Text\a|Tooltip"`.
- *menu*  (`Func<Au.popupMenu>`):
    Func that returns the menu. Called whenever the button clicked.
- *image*  (`Au.Types.MTImage`):
    Image. Read here: `Au.Types.MTBase`.
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Returns

`Au.Types.TBItem`

#### Remarks

The caller creates the menu (creates the `Au.popupMenu` object and adds items) and can reuse it many times. Other overload does not allow to create `Au.popupMenu` and reuse same object. The submenu does not inherit properties of this toolbar.

#### Examples

```
var m = new popupMenu(); m.AddCheck("C1"); m.AddCheck("C2");
t.Menu("Menu", () => m);
```