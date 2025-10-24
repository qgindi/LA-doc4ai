# Method `Au.Types.ExtWpf.RectInScreen`

Gets rectangle of this element in screen coordinates.

```
public static RECT RectInScreen(this FrameworkElement t)
```

##### Parameters

- *t*  (`FrameworkElement`)

##### Returns

`Au.Types.RECT`

`default(RECT)` if this is an invisible element (but not `System.Windows.Window`) or if fails.