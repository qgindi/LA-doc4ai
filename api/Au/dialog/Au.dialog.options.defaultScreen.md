# Property `Au.dialog.options.defaultScreen`

Show dialogs on this screen when screen is not explicitly specified (`Au.dialog.InScreen` or parameter *screen*) and there is no owner window. The `Au.screen` must be lazy or empty.

```
public static screen defaultScreen { get; set; }
```

##### Exceptions

- `ArgumentException`:
    `Au.screen` with `Handle`. Must be lazy or empty.

##### Property Value

`Au.screen`

#### Examples

```
dialog.options.defaultScreen = screen.ofActiveWindow;
dialog.options.defaultScreen = screen.ofMouse;
dialog.options.defaultScreen = screen.at.left(lazy: true);
dialog.options.defaultScreen = screen.index(1, lazy: true);
```