# Property `Au.screen.ScreenIndex`

Gets index of this screen in the `Au.screen.all` array.

```
public int ScreenIndex { get; }
```

##### Property Value

`int`

#### Remarks

Returns 0 (index of primary screen) if this variable is empty. Returns -1 if the screen handle is invalid; it can happen after changing display settings, but is rare.