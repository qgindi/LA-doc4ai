# Enum `Au.Types.PSFormat`

Used with `Au.Types.ParamStringAttribute` to specify string parameter format.

```
public enum PSFormat
```

### Fields

| Name | Description |
| --- | --- |
| CodeFile | Name or path of a script or class file in current workspace. |
| FileInWorkspace | Name or path of any file or folder in current workspace. |
| Hotkey | Hotkey, except triggers. |
| HotkeyTrigger | Hotkey trigger. |
| Keys | Keys. See `Au.keys.send`. |
| NetRegex | .NET regular expression. |
| None |  |
| Regexp | PCRE regular expression. |
| RegexpReplacement | PCRE regular expression replacement string. |
| TriggerMod | Trigger modifiers without key. |
| Wildex | [Wildcard expression](../articles/Wildcard%20expression.html). |