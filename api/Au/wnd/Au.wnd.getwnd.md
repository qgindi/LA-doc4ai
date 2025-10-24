# Struct `Au.wnd.getwnd`

Static functions of this class are used to get special windows (used like `wnd w = wnd.getwnd.top;`) and all windows. Instances of this class are used to get related windows and controls, like `wnd w2 = w1.Get.FirstChild;` (here *w1* is a `Au.wnd` variable).

```
public struct wnd.getwnd
```

### Constructors

`getwnd(wnd)`

### Properties

`DirectParent`, `FirstChild`, `FirstSibling`, `LastChild`, `LastSibling`, `Owner`, `Window`, `root`, `shellWindow`, `top`

### Methods

`AllOwned`, `AllOwners`, `Child`, `Children`, `EnabledOwned`, `LastActiveOwnedOrThis`, `Next`, `Previous`, `RootOwnerOrThis`, `SiblingAbove`, `SiblingAbove`, `SiblingBelow`, `SiblingBelow`, `SiblingLeft`, `SiblingLeft`, `SiblingRight`, `SiblingRight`, `allWindows`, `allWindowsZorder`, `desktop`, `isMainWindow`, `mainWindows`, `nextMain`, `threadWindows`, `top2`