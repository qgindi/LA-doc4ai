# Enum `Au.Types.PrintServerMessageType`

See `Au.Types.PrintServerMessage.Type`.

```
public enum PrintServerMessageType
```

### Fields

| Name | Description |
| --- | --- |
| Clear | Clear the output window. Only `Au.Types.PrintServerMessage.Type` is used. |
| ScrollToTop | Scroll the output window to the top. Only `Au.Types.PrintServerMessage.Type` is used. |
| TaskEvent | Used internally to log events such as start/end of trigger actions. |
| Write | Add line to the output window. All `Au.Types.PrintServerMessage` members can be used. |