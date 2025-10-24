# Method `Au.toolbar.AutoHideScreenEdge`

## Overload 1

Creates a new toolbar and sets its `Au.toolbar.Satellite` = this. Sets properties for showing at a screen edge.

```
public toolbar AutoHideScreenEdge(MouseTriggerArgs mta, Coord rangeStart = default, Coord rangeEnd = default, int thickness = 1, TBCtor ctorFlags = 0, string f_ = null, int l_ = 0)
```

##### Parameters

- *mta*  (`Au.Triggers.MouseTriggerArgs`):
    Mouse edge trigger arguments.
- *rangeStart*  (`Au.Types.Coord`):
    *rangeStart* and *rangeEnd* can be used to specify a smaller range of the edge part. For example, you can create 2 toolbars there: one with 0, .5f, other with .5f, 1f.
- *rangeEnd*  (`Au.Types.Coord`)
- *thickness*  (`int`):
    The visible thickness. Pixels.
- *ctorFlags*  (`Au.Types.TBCtor`):
    `Au.toolbar` constructor flags.
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Returns

`Au.toolbar`

The new toolbar.

* * *

## Overload 2

Creates a new toolbar and sets its `Au.toolbar.Satellite` = this. Sets properties for showing at a screen edge.

```
public toolbar AutoHideScreenEdge(TMEdge edge, screen scrn = default, Coord rangeStart = default, Coord rangeEnd = default, int thickness = 1, TBCtor ctorFlags = 0, string f_ = null, int l_ = 0)
```

##### Parameters

- *edge*  (`Au.Triggers.TMEdge`):
    Screen edge/part.
- *scrn*  (`Au.screen`):
    Screen. Default: primary.
- *rangeStart*  (`Au.Types.Coord`):
    *rangeStart* and *rangeEnd* can be used to specify a smaller range of the edge part. For example, you can create 2 toolbars there: one with 0, .5f, other with .5f, 1f.
- *rangeEnd*  (`Au.Types.Coord`)
- *thickness*  (`int`):
    The visible thickness. Pixels.
- *ctorFlags*  (`Au.Types.TBCtor`):
    `Au.toolbar` constructor flags.
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Returns

`Au.toolbar`

The new toolbar.