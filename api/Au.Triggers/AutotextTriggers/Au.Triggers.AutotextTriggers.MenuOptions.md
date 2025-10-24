# Property `Au.Triggers.AutotextTriggers.MenuOptions`

Options for menus shown by `Au.Triggers.AutotextTriggerArgs.Menu` and `Au.Triggers.AutotextTriggerArgs.Confirm`. Used for triggers added afterwards.

```
public TAMenuOptions MenuOptions { get; set; }
```

##### Property Value

`Au.Triggers.TAMenuOptions`

#### Examples

Show menus by the text cursor. If impossible - in the center of the active window.

```
tt.MenuOptions = new(PMFlags.ByCaret | PMFlags.WindowCenter);
```

### See Also

`Au.popupMenu.caretRectFunc`