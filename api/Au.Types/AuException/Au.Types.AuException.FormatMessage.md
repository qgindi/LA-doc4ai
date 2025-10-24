# Method `Au.Types.AuException.FormatMessage`

Formats error message. Sets and returns `Au.Types.AuException.FormattedMessage`.

```
protected string FormatMessage(string appendMessage = null, string commonPostfix = null)
```

##### Parameters

- *appendMessage*  (`string`)
- *commonPostfix*  (`string`)

##### Returns

`string`

#### Remarks

As base text, uses the text passed to the constructor (default `"Failed."`). If it starts with `"*"`, replaces the `"*"` with `"Failed to "`. If it ends with `"*"`, replaces the `"*"` with *commonPostfix* if it is not empty. If then the message does not end with `"."`, appends `"."`. If *appendMessage* is `null`, uses `lastError.messageFor(NativeErrorCode)` if `Au.Types.AuException.NativeErrorCode` not 0. If then *appendMessage* is not empty, appends `" " + appendMessage`. Also appends `InnerException.Message` in new tab-indented line if `System.Exception.InnerException` is not `null`.