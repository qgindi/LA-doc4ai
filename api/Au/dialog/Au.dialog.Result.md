# Property `Au.dialog.Result`

Selected button id. The same as the `Au.dialog.ShowDialog` return value.

```
public int Result { get; }
```

##### Property Value

`int`

#### Remarks

If the result is still unavailable (the dialog still not closed):

- If called from the same thread that called `Au.dialog.ShowDialog`, returns 0.
- If called from another thread, waits until the dialog is closed.

Note: `Au.dialog.ShowDialogNoWait` calls `Au.dialog.ShowDialog` in another thread.