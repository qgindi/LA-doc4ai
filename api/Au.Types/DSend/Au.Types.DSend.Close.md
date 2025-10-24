# Method `Au.Types.DSend.Close`

Clicks a button. Normally it closes the dialog.

```
public bool Close(int buttonId = 0)
```

##### Parameters

- *buttonId*  (`int`):
    A button id or some other number that will be returned by `Au.dialog.ShowDialog`.

##### Returns

`bool`

#### Remarks

Call this method while the dialog is open, eg in an event handler. Sends message `Au.Types.DNative.TDM.CLICK_BUTTON`.