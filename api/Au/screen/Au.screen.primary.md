# Property `Au.screen.primary`

Gets the primary screen.

```csharp
public static screen primary { get; }
```

##### Property Value

`Au.screen`

#### Remarks

The returned variable has `Au.screen.Handle`. To create lazy variable (with `Au.screen.LazyFunc`), use `screen.index(0, lazy: true)`.