# Property `Au.screen.Info`

Gets screen rectangle and other info.

```
public (RECT rect, RECT workArea, bool isPrimary, bool isAlive) Info { get; }
```

##### Property Value

`(RECT rect, RECT workArea, bool isPrimary, bool isAlive)`

Tuple containing:

- `rect` - screen rectangle.
- `workArea` - work area rectangle.
- `isPrimary` - `true` if it is the primary screen.
- `isAlive` - `false` if the screen handle is invalid; then the function gets info of the primary screen.

#### Remarks

If this variable holds a callback function, this function calls it to get screen handle. See also `Au.screen.Now`.