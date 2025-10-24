# Method `Au.osdText.showTransparentText`

Shows a big-font text with transparent background.

```
public static osdText showTransparentText(string text, int secondsTimeout = 0, PopupXY xy = null, ColorInt? color = null, FontNSS font = null, string name = null, OsdMode showMode = OsdMode.Auto, bool dontShow = false)
```

##### Parameters

- *text*  (`string`):
    Text in OSD window.
Sets `Au.osdText.Text`.
- *secondsTimeout*  (`int`):
    Close the OSD window after this time, seconds. If 0 (default), depends on text length. Can be `System.Threading.Timeout.Infinite` (-1). Sets `Au.osdText.SecondsTimeout`.
- *xy*  (`Au.Types.PopupXY`):
    Coordinates. Default: `null` (screen center). Sets `Au.osdText.XY`.
- *color*  (`Au.Types.ColorInt?`):
    Sets `Au.osdText.TextColor`. Default: `Au.osdText.defaultTransparentTextColor`.
- *font*  (`Au.Types.FontNSS`):
    Sets `Au.osdText.Font`. Default: `Au.osdText.defaultBigFont`.
- *name*  (`string`):
    OSD window name.
Sets `Au.Types.OsdWindow.Name`.
- *showMode*  (`Au.Types.OsdMode`):
    Sets `Au.osdText.ShowMode`.
- *dontShow*  (`bool`):
    Don't call `Au.osdText.Show`. The caller can use the return value to set some other properties and call `Show`.

##### Returns

`Au.osdText`

Returns an `Au.osdText` object that can be used to change properties or close the OSD window.

#### Remarks

Also sets these properties: `Au.Types.OsdWindow.Opacity`=0.