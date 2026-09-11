# Method `Au.Types.DSend.Message`

Sends a message to the dialog.

```csharp
public int Message(DNative.TDM message, nint wParam = 0, nint lParam = 0)
```

##### Parameters

- *message*  (`Au.Types.DNative`.`Au.Types.DNative.TDM`):
  Enum: NAVIGATE_PAGE, CLICK_BUTTON, SET_MARQUEE_PROGRESS_BAR, SET_PROGRESS_BAR_STATE, SET_PROGRESS_BAR_RANGE, SET_PROGRESS_BAR_POS, SET_PROGRESS_BAR_MARQUEE, SET_ELEMENT_TEXT, CLICK_RADIO_BUTTON, ENABLE_BUTTON, ENABLE_RADIO_BUTTON, CLICK_VERIFICATION, UPDATE_ELEMENT_TEXT, SET_BUTTON_ELEVATION_REQUIRED_STATE, UPDATE_ICON.
- *wParam*  (`nint`)
- *lParam*  (`nint`)

##### Returns

`int`

#### Remarks

Call this method while the dialog is open, eg in an event handler.
Example (in an event handler):`e.d.Send.Message(DNative.TDM.CLICK_VERIFICATION, 1);`Also there are several other functions to send some messages: change text, close dialog, enable/disable buttons, update progress.
Reference:[task dialog messages](🔗).
`NAVIGATE_PAGE` not supported.