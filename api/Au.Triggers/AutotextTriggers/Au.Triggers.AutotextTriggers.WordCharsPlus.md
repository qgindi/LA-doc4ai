# Property `Au.Triggers.AutotextTriggers.WordCharsPlus`

Additional word characters (non-delimiters). Default: `null`.

```
public string WordCharsPlus { get; set; }
```

##### Property Value

`string`

#### Remarks

By default, only alpha-numeric characters (`char.IsLetterOrDigit` returns `true`) are considered word characters. You can use this property to add more word characters, for example `"_#"`. This is used to avoid activating triggers when a trigger text found inside a word. This property is applied to all triggers, not just to those added afterwards.