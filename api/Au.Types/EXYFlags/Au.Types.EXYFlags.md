# Enum `Au.Types.EXYFlags`

Flags for `Au.elm.fromXY`.

```
[Flags]
public enum EXYFlags
```

### Fields

| Name | Description |
| --- | --- |
| NotInProc | Don't load dll into the target process. More info: `Au.Types.EFFlags.NotInProc`. |
| OrUIA | Use UI Automation API if the default API fails and in some other cases. The **Find UI element** tool uses this flag when `UIA` is in indeterminate state. |
| PreferLink | Get the direct parent UI element if probably it would be much more useful, for example if its role is `LINK` or `BUTTON`. Usually links have one or more children of type `TEXT`, `STATICTEXT`, `IMAGE` or other. |
| TrySmaller |  |
| UIA | Use UI Automation API. More info: `Au.Types.EFFlags.UIA`. |