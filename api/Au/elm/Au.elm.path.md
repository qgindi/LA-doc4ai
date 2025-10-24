# Property `Au.elm.path`

Gets an `Au.elmFinder` for finding UI elements in a window or UI element that can be set later with `Au.elmFinder.In`. Example: `var e = elm.path["ROLE", "Name"].In(w).Find();`. Same as `var e = w.Elm["ROLE", "Name"].Find();`. Example: `var e = elm.path["ROLE1", "Name1"]["ROLE2", "Name2"]["ROLE3", "Name3"].In(w).Find();`.

```
public static elmFinder path { get; }
```

##### Property Value

`Au.elmFinder`

### See Also

this[`elmFinder.this[]`, `string`, `Au.Types.Strings`, `Au.Types.EFFlags`, `Func<Au.elm, bool>`, `int`, `string`]