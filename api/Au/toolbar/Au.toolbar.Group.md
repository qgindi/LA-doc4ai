# Method `Au.toolbar.Group`

Adds new horizontal separator, optionally with text.

```
public TBItem Group(string text = null)
```

##### Parameters

- *text*  (`string`):
    Text. Or `"Text|Tooltip"`, or `"|Tooltip"`, or `"Text|"`. Separator can be `"|"` or `"\0 "` (then `"|"` isn't a separator).

##### Returns

`Au.Types.TBItem`