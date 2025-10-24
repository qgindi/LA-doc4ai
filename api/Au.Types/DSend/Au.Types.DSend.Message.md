# Method `Au.Types.DSend.Message`

Sends a message to the dialog.

```
public int Message(DNative.TDM message, nint wParam = 0, nint lParam = 0)
```

##### Parameters

- *message*  (`Au.Types.DNative`.`Au.Types.DNative.TDM`)
- *wParam*  (`nint`)
- *lParam*  (`nint`)

##### Returns

`int`

#### Remarks

Call this method while the dialog is open, eg in an event handler. Example (in an event handler): `e.d.Send.Message(DNative.TDM.CLICK_VERIFICATION, 1);` Also there are several other functions to send some messages: change text, close dialog, enable/disable buttons, update progress. Reference: [task dialog messages](https://www.google.com/search?q=task+dialog+messages+site:microsoft.com). `NAVIGATE_PAGE` not supported.