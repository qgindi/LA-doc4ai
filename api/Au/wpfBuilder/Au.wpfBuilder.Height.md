# Method `Au.wpfBuilder.Height`

Sets height of the last added element. Optionally sets alignment.

```
public wpfBuilder Height(WBLength height, string alignY = null)
```

##### Parameters

- *height*  (`Au.Types.WBLength`):
    Height or/and min/max height.
- *alignY*  (`string`):
    Vertical alignment. If not `null`, calls `Au.wpfBuilder.Align`.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `ArgumentException`:
    Invalid alignment string.