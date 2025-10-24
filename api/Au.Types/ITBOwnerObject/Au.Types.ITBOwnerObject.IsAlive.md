# Property `Au.Types.ITBOwnerObject.IsAlive`

Returns `false` to close the toolbar.

```
bool IsAlive { get; }
```

##### Property Value

`bool`

#### Remarks

Not called if the owner window is invisible or cloaked or minimized. The default implementation returns `true`.