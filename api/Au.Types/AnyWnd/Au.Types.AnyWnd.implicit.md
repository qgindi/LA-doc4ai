# Operator `Au.Types.AnyWnd.implicit operator`

## Overload 1

Assignment of a value of type `Au.wnd`.

```
public static implicit operator AnyWnd(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`)

##### Returns

`Au.Types.AnyWnd`

* * *

## Overload 2

Assignment of a window handle as `IntPtr`.

```
public static implicit operator AnyWnd(nint hwnd)
```

##### Parameters

- *hwnd*  (`nint`)

##### Returns

`Au.Types.AnyWnd`

* * *

## Overload 3

Assignment of a value of type `System.Windows.Forms.Control` (`Form` or any control class).

```
public static implicit operator AnyWnd(Control c)
```

##### Parameters

- *c*  (`Control`)

##### Returns

`Au.Types.AnyWnd`

* * *

## Overload 4

Assignment of a value of type `System.Windows.DependencyObject` (WPF window or control).

```
public static implicit operator AnyWnd(DependencyObject c)
```

##### Parameters

- *c*  (`DependencyObject`)

##### Returns

`Au.Types.AnyWnd`