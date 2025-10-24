# Enum `Au.Types.EMiscFlags`

Flags returned by `Au.elm.MiscFlags`.

```
[Flags]
public enum EMiscFlags : byte
```

### Fields

| Name | Description |
| --- | --- |
| InProc | This UI element was retrieved by the dll loaded into its process. More info: `Au.Types.EFFlags.NotInProc`. |
| Java | This UI element was retrieved using Java Access Bridge API. More info: `Au.elm`. |
| UIA | This UI element was retrieved using UI Automation API. More info: `Au.Types.EFFlags.UIA`. |