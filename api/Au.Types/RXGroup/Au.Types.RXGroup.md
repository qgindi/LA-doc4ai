# Struct `Au.Types.RXGroup`

Regular expression group match info. Used with `Au.Types.RXMatch`, `Au.regexp` and some `System.String` extension methods.

```
public struct RXGroup
```

##### Remarks

Groups are regular expression parts enclosed in `()`. Except non-capturing parts, like `(?:...)` and `(?options)`. A `RXGroup` variable contains info about a group found in the subject string: index, length, substring.

Some groups specified in regular expression may not exist in the subject string even if it matches the regular expression. For example, regular expression `"A(\d+)?B"` matches string `"AB"`, but group `(\d+)` does not exist. Then `Au.Types.RXGroup.Exists` is `false`, `Au.Types.RXGroup.Start` -1, `Au.Types.RXGroup.Length` 0, `Au.Types.RXGroup.Value` `null`.

When a group matches multiple times, the `RXGroup` variable contains only the last instance. For example, if subject is `"begin 12 345 67 end"` and regular expression is `(\d+ )+`, value of group 1 is `"67"`. If you need all instances (`"12"`, `"345"`, `"67"`), instead use .NET `System.Text.RegularExpressions.Regex` and `System.Text.RegularExpressions.Group.Captures`. Also you can get all instances with `Au.regexp.Callout`.

Examples and more info: `Au.Types.RXMatch`, `Au.regexp`.

### Properties

`End`, `Exists`, `Length`, `Span`, `Start`, `Value`

### Methods

`ToString`

### Operators

`implicit operator Range(RXGroup)`