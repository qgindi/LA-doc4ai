# Property `Au.elm.IsInvisible`

Calls `Au.elm.State` and returns `true` if has state `INVISIBLE` and does not have state `OFFSCREEN`.

```
public bool IsInvisible { get; }
```

##### Property Value

`bool`

#### Remarks

If the UI element has both `INVISIBLE` and `OFFSCREEN` states, it is either invisible or just offscreen, depending on application etc. Then this function works like `Au.elmFinder.Find` and similar functions: for most UI elements returns `false` (is visible), but for UI elements that have these roles returns `true` (invisible): `WINDOW`, `DOCUMENT`, `PROPERTYPAGE`, `GROUPING`, `ALERT`, `MENUPOPUP`. Does not check whether this UI element is in an invisible parent/ancestor UI element.