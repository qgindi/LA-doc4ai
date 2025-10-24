# Enum `Au.Types.PNFlags`

Flags for `Au.pathname.normalize`.

```
[Flags]
public enum PNFlags
```

### Fields

| Name | Description |
| --- | --- |
| CanBeUrlOrShell | If path is not a file-system path but looks like URL (eg `"http:..."` or `"file:..."`) or starts with `"::"`, don't throw exception and don't process more (only expand environment variables). |
| DontExpandDosPath | Don't call API `GetLongPathName`. |
| DontPrefixLongPath | Don't call `Au.pathname.prefixLongPathIfNeed`. |
| DontRemoveEndSeparator | Don't remove `\` character at the end. |