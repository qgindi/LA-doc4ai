# Method `Au.toolbar.Hide`

Adds or removes a reason to temporarily hide the toolbar. The toolbar is hidden if at least one reason exists. See also `Au.toolbar.Close`.

```
public void Hide(bool hide, TBHide reason)
```

##### Parameters

- *hide*  (`bool`):
    `true` to hide (add *reason*), `false` to show (remove *reason*).
- *reason*  (`Au.Types.TBHide`):
    A user-defined reason to hide/unhide. Can be `Au.Types.TBHide.User` or a bigger value, eg `(TBHide)0x20000`, `(TBHide)0x40000`.

##### Exceptions

- `InvalidOperationException`:

    - The toolbar was never shown (`Au.toolbar.Show` not called).
    - It is a satellite toolbar.
    - Wrong thread. Must be called from the same thread that created the toolbar. See `Au.Types.MTBase.ActionThread`.
- `ArgumentOutOfRangeException`:
    *reason* is less than `Au.Types.TBHide.User`.

#### Remarks

Toolbars are automatically hidden when the owner window is hidden, minimized, etc. This function can be used to hide toolbars for other reasons.