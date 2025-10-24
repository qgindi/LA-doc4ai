# Method `Au.toolbar.AutoHide`

Creates a new toolbar and sets its `Au.toolbar.Satellite` = this.

```
public toolbar AutoHide(TBCtor ctorFlags = 0, string f_ = null, int l_ = 0)
```

##### Parameters

- *ctorFlags*  (`Au.Types.TBCtor`):
    `Au.toolbar` constructor flags.
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Returns

`Au.toolbar`

The new toolbar.

##### Exceptions

- `InvalidOperationException`:
    This toolbar was attached to another toolbar or was shown as non-satellite toolbar.

#### Remarks

Sets toolbar name = `this.Name + "^"`. If this already is a satellite toolbar, just returns its owner.