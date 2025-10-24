# Method `Au.wpfBuilder.Size`

Sets width and height of the last added element. Optionally sets alignment.

```
public wpfBuilder Size(WBLength width, WBLength height, string alignX = null, string alignY = null)
```

##### Parameters

- *width*  (`Au.Types.WBLength`):
    Width or/and min/max width.
- *height*  (`Au.Types.WBLength`):
    Height or/and min/max height.
- *alignX*  (`string`):
    Horizontal alignment. If not `null`, calls `Au.wpfBuilder.Align`.
- *alignY*  (`string`):
    Vertical alignment.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `ArgumentException`:
    Invalid alignment string.