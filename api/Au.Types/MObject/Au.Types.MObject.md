# Struct `Au.Types.MObject`

This type is used for parameters of `Au.mouse` functions that accept multiple types of UI objects (window, UI element, screen, etc).

```
public struct MObject
```

##### Remarks

Has implicit conversions from `Au.wnd`, `Au.elm`, `Au.uiimage`, `Au.screen`, `Au.Types.RECT` and `bool` (relative coordinates). Also has static functions to specify more parameters.

### Properties

`Value`

### Methods

`RectInWindow`, `Screen`, `Window`

### Operators

`implicit operator MObject(RECT)`, `implicit operator MObject(elm)`, `implicit operator MObject(screen)`, `implicit operator MObject(uiimage)`, `implicit operator MObject(wnd)`, `implicit operator MObject(bool)`