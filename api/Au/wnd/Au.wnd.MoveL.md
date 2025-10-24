# Method `Au.wnd.MoveL`

## Overload 1

Moves and resizes.

```
public bool MoveL(int x, int y, int width, int height, SWPFlags swpFlagsToAdd = 0)
```

##### Parameters

- *x*  (`int`)
- *y*  (`int`)
- *width*  (`int`)
- *height*  (`int`)
- *swpFlagsToAdd*  (`Au.Types.SWPFlags`)

##### Returns

`bool`

#### Remarks

See also `Au.wnd.Move`. It is better to use in automation scripts, with windows of any process/thread. It throws exceptions, supports optional/reverse/fractional/workarea coordinates, restores if min/max, does not support `SWP` flags. This function is more lightweight, it just calls API `SetWindowPos` with flags `NOZORDER|NOOWNERZORDER|NOACTIVATE|swpFlagsToAdd`. It is better to use in programming, with windows of current thread. Supports `Au.lastError`.

For top-level windows use screen coordinates. For controls - direct parent client coordinates.

### See Also

`Au.wnd.SetWindowPos`

* * *

## Overload 2

Moves and resizes. Same as `Au.wnd.MoveL(int, int, int, int, SWPFlags)`.

```
public bool MoveL(RECT r, SWPFlags swpFlagsToAdd = 0, bool visibleRect = false)
```

##### Parameters

- *r*  (`Au.Types.RECT`)
- *swpFlagsToAdd*  (`Au.Types.SWPFlags`)
- *visibleRect*  (`bool`):
    Use the visible rectangle without the transparent frame. Note: the window should be visible. This parameter not used with child windows.

##### Returns

`bool`

* * *

## Overload 3

Moves.

```
public bool MoveL(int x, int y)
```

##### Parameters

- *x*  (`int`)
- *y*  (`int`)

##### Returns

`bool`

#### Remarks

See also `Au.wnd.Move`. It is better to use in automation scripts, with windows of any process/thread. It throws exceptions, supports optional/reverse/fractional/workarea coordinates, restores if min/max. This function is more lightweight, it just calls API `SetWindowPos` with flags `NOSIZE|NOZORDER|NOOWNERZORDER|NOACTIVATE`. It is better to use in programming, with windows of current thread. Supports `Au.lastError`.

For top-level windows use screen coordinates. For controls - direct parent client coordinates.

### See Also

`Au.wnd.SetWindowPos`