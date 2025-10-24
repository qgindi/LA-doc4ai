# Indexer of `Au.toolbar`

Adds button. Same as `Au.toolbar.Add`.

```
public Action<TBItem> this[string text, MTImage image = default, int l_ = 0, string f_ = null] { set; }
```

##### Parameters

- *text*  (`string`):
    Text. Or `"Text|Tooltip"`, or `"|Tooltip"`, or `"Text|"`. Separator can be `"|"` or `"\0 "` (then `"|"` isn't a separator). To always display text regardless of `Au.toolbar.DisplayText`, append `"\a"`, like `"Text\a"` or `"Text\a|Tooltip"`.
- *image*  (`Au.Types.MTImage`):
    Image. Read here: `Au.Types.MTBase`.
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Property Value

`Action<Au.Types.TBItem>`

Action called when the button clicked.

#### Remarks

More properties can be specified later (set properties of `Au.toolbar.Last` `Au.Types.TBItem` or use `Au.toolbar.Items`) or before (`Au.Types.MTBase.ActionThread`, `Au.Types.MTBase.ActionException`, `Au.Types.MTBase.ExtractIconPathFromCode`, `Au.Types.MTBase.PathInTooltip`).

#### Examples

These two are the same.

```
tb.Add("Example", o => print.it(o));
tb["Example"] = o => print.it(o);
```

These four are the same.

```
var b = tb.Add("Example", o => print.it(o)); b.Tooltip="tt";
tb.Add("Example", o => print.it(o)).Tooltip="tt";
tb["Example"] = o => print.it(o); var b=tb.Last; b.Tooltip="tt";
tb["Example"] = o => print.it(o); tb.Last.Tooltip="tt";
```