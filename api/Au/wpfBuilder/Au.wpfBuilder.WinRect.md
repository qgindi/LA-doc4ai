# Method `Au.wpfBuilder.WinRect`

Sets window rectangle (location and size).

```
public wpfBuilder WinRect(RECT r)
```

##### Parameters

- *r*  (`Au.Types.RECT`):
    Rectangle in screen. Physical pixels.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:

    - Container is not of type `Window`.
    - Cannot be after `Au.wpfBuilder.WinXY`, `Au.wpfBuilder.WinRect(RECT)` or `Au.wpfBuilder.WinSaved`.

#### Remarks

With this function use physical pixels, not WPF logical device-independent units. Call this function before showing the window. Don't change location/size-related window properties after that. Calls `Au.Types.ExtWpf.SetRect`.

### See Also

`Au.wpfBuilder.WinSaved`