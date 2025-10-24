# Method `Au.Types.HookData.ReplyMessage`

Calls API API `ReplyMessage`, which allows to use `Au.elm` and COM in the hook procedure.

```
public static void ReplyMessage(bool cancelEvent)
```

##### Parameters

- *cancelEvent*  (`bool`):
    Don't notify the target window about the event, and don't call other hook procedures. This value is used instead of the return value of the hook procedure, which is ignored.

#### Remarks

It can be used as a workaround for this problem: in low-level hook procedure some functions don't work with some windows. For example cannot get a UI element or use a COM object. Error/exception "An outgoing call cannot be made since the application is dispatching an input-synchronous call (0x8001010D)".