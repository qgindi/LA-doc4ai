# Method `Au.dialog.XY`

Sets dialog position in screen.

```
public dialog XY(Coord x, Coord y, bool rawXY = false)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X position in screen. If `default` - screen center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y position in screen. If `default` - screen center.
- *rawXY*  (`bool`):
    *x y* are relative to the primary screen (ignore `Au.dialog.InScreen` etc).

##### Returns

`Au.dialog`

### See Also

`Au.dialog.InScreen`