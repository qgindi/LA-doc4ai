# Constructor of `Au.Triggers.TAMenuItem`

Sets menu item label and replacement text.

```
public TAMenuItem(string label, string text, string html = null, int l_ = 0)
```

##### Parameters

- *label*  (`string`):
    Menu item label. If `null`, uses `Au.Triggers.TAMenuItem.Text`. Can contain tooltip like `"Label\0 Tooltip"`.
- *text*  (`string`):
    The replacement text. Can be `null`. Can contain caret placeholder `[[|]]`. See `Au.Triggers.AutotextTriggerArgs.Replace`.
- *html*  (`string`):
    The replacement HTML. Can be `null`. See `Au.Triggers.AutotextTriggerArgs.Replace`.
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)