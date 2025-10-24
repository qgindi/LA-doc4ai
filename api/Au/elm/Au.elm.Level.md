# Property `Au.elm.Level`

Gets or sets indentation level for `Au.elm.ToString`.

```
public int Level { get; set; }
```

##### Property Value

`int`

#### Remarks

When `Au.elmFinder.Find` or similar function finds a UI element, it sets this property of the `Au.elm` variable. If `Au.elm.fromXY` etc, it is 0 (unknown). When searching in a window, at level 0 are direct children of the `WINDOW`. When searching in controls (specified class or id), at level 0 is the control. When searching in `Au.elm`, at level 0 are its direct children. When searching in web page (role prefix `"web:"` etc), at level 0 is the web page (role `DOCUMENT` or `PANE`).