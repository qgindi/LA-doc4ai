# Property `Au.Types.RXGroup.Value`

Gets substring of the subject string from `Au.Types.RXGroup.Start` to `Au.Types.RXGroup.End`.

```
public string Value { get; }
```

##### Property Value

`string`

`null` if the group does not exist in the subject string (see `Au.Types.RXGroup.Exists`).

#### Remarks

Creates new string each time. See also `Au.Types.RXGroup.Span`.