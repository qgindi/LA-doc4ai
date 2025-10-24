# Method `Au.Types.DSend.EnableButton`

Enables or disables a button.

```
public void EnableButton(int buttonId, bool enable)
```

##### Parameters

- *buttonId*  (`int`)
- *enable*  (`bool`)

#### Remarks

Call this method while the dialog is open, eg in an event handler. Example: `d.Created += e => { e.d.Send.EnableButton(4, false); };` Sends message `Au.Types.DNative.TDM.ENABLE_BUTTON`.