# Enum `Au.Types.EFocusedFlags`

Flags for `Au.elm.focused`.

```
[Flags]
public enum EFocusedFlags
```

### Fields

| Name | Description |
| --- | --- |
| NotInProc | Don't load dll into the target process. More info: `Au.Types.EFFlags.NotInProc`. |
| UIA | Use UI Automation API. Need this flag with some windows that don't support accessible objects but support UI Automation elements. Can be used with most other windows too. More info: `Au.Types.EFFlags.UIA`. |