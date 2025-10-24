# Method `Au.wpfBuilder.WinSize`

Sets window width and/or height or/and min/max width/height.

```
public wpfBuilder WinSize(WBLength? width = null, WBLength? height = null)
```

##### Parameters

- *width*  (`Au.Types.WBLength?`):
    Width or/and min/max width.
- *height*  (`Au.Types.WBLength?`):
    Height or/and min/max height.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:

    - Container is not of type `Window`.
    - Cannot be after the last `Au.wpfBuilder.End`.
    - Cannot be after `Au.wpfBuilder.WinRect` or `Au.wpfBuilder.WinSaved`.

#### Remarks

Use WPF logical device-independent units, not physical pixels.

### See Also

`Au.wpfBuilder.WinRect`

`Au.wpfBuilder.WinSaved`