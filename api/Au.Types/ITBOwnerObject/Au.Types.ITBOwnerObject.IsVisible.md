# Property `Au.Types.ITBOwnerObject.IsVisible`

Returns `false` to hide the toolbar temporarily.

```
bool IsVisible { get; }
```

##### Property Value

`bool`

#### Remarks

Not called if the owner window is invisible or cloaked or minimized. The default implementation returns `true`.