# Method `Au.wpfBuilder.Width`

Sets width of the last added element. Optionally sets alignment.

```
public wpfBuilder Width(WBLength width, string alignX = null)
```

##### Parameters

- *width*  (`Au.Types.WBLength`):
    Width or/and min/max width.
- *alignX*  (`string`):
    Horizontal alignment. If not `null`, calls `Au.wpfBuilder.Align`.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `ArgumentException`:
    Invalid alignment string.