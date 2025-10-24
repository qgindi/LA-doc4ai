# Property `Au.screen.Now`

Returns a copy of this variable with `Au.screen.Handle`.

```
public screen Now { get; }
```

##### Property Value

`Au.screen`

#### Remarks

If this variable has `Au.screen.Handle`, returns its clone. Else if has `Au.screen.LazyFunc`, calls it. Else gets the primary screen.