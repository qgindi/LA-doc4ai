# Property `Au.Types.RXGroup.Exists`

Returns `true` if the group exists in the subject string, `false` if does not exist. More info in `Au.Types.RXGroup` topic. Example in `Au.Types.RXMatch` topic.

```
public bool Exists { get; }
```

##### Property Value

`bool`

#### Remarks

Other ways to detect it: if a group does not exist, its `Au.Types.RXGroup.Start` is -1 and `Au.Types.RXGroup.Value` is `null`.