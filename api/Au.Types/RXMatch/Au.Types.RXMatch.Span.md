# Property `Au.Types.RXMatch.Span`

Gets span of the subject string from `Au.Types.RXMatch.Start` to `Au.Types.RXMatch.End`. The same as that of group 0 (`Au.Types.RXGroup.Span`).

```
public ReadOnlySpan<char> Span { get; }
```

##### Property Value

`ReadOnlySpan<char>`

#### Remarks

Unlike `Au.Types.RXMatch.Value`, does not create new string.