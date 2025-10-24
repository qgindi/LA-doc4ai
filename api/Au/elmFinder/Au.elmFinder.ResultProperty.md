# Property `Au.elmFinder.ResultProperty`

The requested property of the found UI element, depending on `Au.elmFinder.ResultGetProperty`. `null` if: 1. UI element not found. 2. `ResultGetProperty` not used or is `'-'`. 3. Failed to get the property.

```
public object ResultProperty { get; }
```

##### Property Value

`object`

#### Remarks

The type depends on the property. Most properties are of type `String`. Others: `Au.elm.Rect`, `Au.elm.State`, `Au.elm.WndContainer`, `Au.elm.HtmlAttributes`.