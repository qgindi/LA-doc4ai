# Method `Au.More.WndUtil.RegisterMessage`

Calls API `RegisterWindowMessage`.

```
public static int RegisterMessage(string name, bool uacEnable = false)
```

##### Parameters

- *name*  (`string`):
    Message name. Can be any unique string.
- *uacEnable*  (`bool`):
    Also call API `ChangeWindowMessageFilter` for the message. More info: `Au.More.WndUtil.UacEnableMessages`.

##### Returns

`int`