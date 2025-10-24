# Property `Au.Types.RXGroup.Span`

Gets span of the subject string from `Au.Types.RXGroup.Start` to `Au.Types.RXGroup.End`.

```
public ReadOnlySpan<char> Span { get; }
```

##### Property Value

`ReadOnlySpan<char>`

`default` if the group does not exist in the subject string (see `Au.Types.RXGroup.Exists`).

#### Remarks

Unlike `Au.Types.RXGroup.Value`, does not create new string.