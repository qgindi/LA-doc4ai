# Method `Au.elm.ToString`

Formats string from main properties of this UI element.

```
public override string ToString()
```

##### Returns

`string`

##### Overrides

`object.ToString()`

#### Remarks

The string starts with role. Other properties have format like `x="value"`, where `x` is a property character like with `Au.elm.GetProperties`; character `e` is `Au.elm.Item`. HTML attributes have format `@name="value"`. In string values are used C# escape sequences, for example `\r\n` for new line. Indentation depends on `Au.elm.Level`.