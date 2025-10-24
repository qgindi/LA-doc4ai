# Class `Au.Types.DEventArgs`

Arguments for `Au.dialog` event handlers.

```
public record DEventArgs : IEquatable<DEventArgs>
```

##### Remarks

To return a non-zero value from the callback function, assign the value to the `returnValue` field. More info: `TaskDialogCallbackProc`.

##### Inheritance

`object` → `DEventArgs`

### Constructors

`DEventArgs(dialog, wnd, TDN, nint, int, int, string)`

### Fields

`returnValue`

### Properties

`Button`, `DontCloseDialog`, `EditText`, `LinkHref`, `TimerTimeMS`, `d`, `hwnd`, `message`, `wParam`