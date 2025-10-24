# Method `Au.wpfBuilder.WinXY`

Sets window location.

```
public wpfBuilder WinXY(int x, int y)
```

##### Parameters

- *x*  (`int`):
    X coordinate in screen. Physical pixels.
- *y*  (`int`):
    Y coordinate in screen. Physical pixels.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:

    - Container is not of type `Window`.
    - Cannot be after `Au.wpfBuilder.WinXY(int, int)`, `Au.wpfBuilder.WinRect` or `Au.wpfBuilder.WinSaved`.

#### Remarks

With this function use physical pixels, not WPF logical device-independent units. Call this function before showing the window. Don't change location/size-related window properties after that. Calls `Au.Types.ExtWpf.SetXY`.

### See Also

`Au.wpfBuilder.WinSaved`