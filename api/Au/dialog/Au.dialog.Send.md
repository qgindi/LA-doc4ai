# Property `Au.dialog.Send`

Allows to modify dialog controls while it is open, and close the dialog.

```
public DSend Send { get; }
```

##### Property Value

`Au.Types.DSend`

#### Remarks

Example: `d.Send.Close();` . Example: `d.Send.ChangeText2("new text", false);` . Example: `d.Send.Message(DNative.TDM.CLICK_VERIFICATION, 1);` .

Can be used only while the dialog is open. Before showing the dialog returns `null`. After closing the dialog the returned variable is deactivated; its method calls are ignored. Can be used in dialog event handlers. Also can be used in another thread, for example with `Au.dialog.showNoWait` and `Au.dialog.showProgress`.