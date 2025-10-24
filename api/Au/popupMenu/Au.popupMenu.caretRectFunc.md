# Property `Au.popupMenu.caretRectFunc`

Sets a user-defined "get caret rectangle" function.

```
public static Func<RECT?> caretRectFunc { get; set; }
```

##### Property Value

`Func<Au.Types.RECT?>`

Default: null; calls `Au.miscInfo.getTextCursorRect`.

#### Remarks

The callback function is called by `Au.popupMenu.Show` when *flags* includes `Au.Types.PMFlags.ByCaret`. Also used by `Au.Triggers.AutotextTriggerArgs.Menu`. Let it return a rectangle in screen, or null if failed. For example, it can call `Au.miscInfo.getTextCursorRect`; if it fails, use an alternative way to get caret rectangle or preferred menu location.