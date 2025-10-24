# Method `Au.wnd.ThrowNoNative`

Throws `Au.Types.AuWndException` that uses *mainMessage* and does not use the last Windows API error. Also the message depends on whether the window handle is 0/invalid.

```
public void ThrowNoNative(string mainMessage)
```

##### Parameters

- *mainMessage*  (`string`)

##### Exceptions

- `Au.Types.AuWndException`