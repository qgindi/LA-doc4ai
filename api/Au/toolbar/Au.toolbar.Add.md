# Method `Au.toolbar.Add`

Adds button. Same as `Au.toolbar.this[]`.

```
public TBItem Add(string text, Action<TBItem> click, MTImage image = default, int l_ = 0, string f_ = null)
```

##### Parameters

- *text*  (`string`):
    Text. Or `"Text|Tooltip"`, or `"|Tooltip"`, or `"Text|"`. Separator can be `"|"` or `"\0 "` (then `"|"` isn't a separator). To always display text regardless of `Au.toolbar.DisplayText`, append `"\a"`, like `"Text\a"` or `"Text\a|Tooltip"`.
- *click*  (`Action<Au.Types.TBItem>`):
    Action called when the button clicked.
- *image*  (`Au.Types.MTImage`):
    Image. Read here: `Au.Types.MTBase`.
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Returns

`Au.Types.TBItem`

#### Remarks

More properties can be specified later (set properties of the returned `Au.Types.TBItem` or use `Au.toolbar.Items`) or before (`Au.Types.MTBase.ActionThread`, `Au.Types.MTBase.ActionException`, `Au.Types.MTBase.ExtractIconPathFromCode`, `Au.Types.MTBase.PathInTooltip`).