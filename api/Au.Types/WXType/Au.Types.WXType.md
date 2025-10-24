# Enum `Au.Types.WXType`

The type of text (wildcard expression) of a `Au.wildex` variable.

```
public enum WXType : byte
```

### Fields

| Name | Description |
| --- | --- |
| Error | The regular expression was invalid, and parameter *noException* `true`. |
| Multi | Multiple parts (option `m`). `Au.wildex.Match` calls `Match` for each part (see `Au.wildex.MultiArray`) and returns `true` if all negative (option `n`) parts return `true` (or there are no such parts) and some positive (no option `n`) part returns `true` (or there are no such parts). If you want to implement a different logic, call `Match` for each `Au.wildex.MultiArray` element (instead of calling `Match` for this variable). |
| RegexNet | .NET regular expression (option `R`). `Au.wildex.Match` calls `System.Text.RegularExpressions.Regex.IsMatch`. |
| RegexPcre | PCRE regular expression (option `r`). `Au.wildex.Match` calls `Au.regexp.IsMatch`. |
| Text | Simple text (option `t`, or no `*?` characters and no `t`, `r`, `R` options). |
| Wildcard | Wildcard (has `*?` characters and no `t`, `r`, `R` options). `Au.wildex.Match` calls `Au.Types.ExtString.Like`. |