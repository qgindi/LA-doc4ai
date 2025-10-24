# Method `Au.Types.ITBOwnerObject.GetRect`

Gets object rectangle.

```
bool GetRect(out RECT r)
```

##### Parameters

- *r*  (`Au.Types.RECT`):
    Rectangle in screen coordinates.

##### Returns

`bool`

`false` if failed.

#### Remarks

Not called if the owner window is invisible or cloaked or minimized or if `Au.Types.ITBOwnerObject.IsVisible` returned `false`.