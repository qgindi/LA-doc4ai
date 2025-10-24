# Method `Au.osdText.showText`

Shows a tooltip-like OSD window with text and optionally icon.

```
public static osdText showText(string text, int secondsTimeout = 0, PopupXY xy = null, object icon = null, ColorInt? textColor = null, ColorInt? backColor = null, FontNSS font = null, string name = null, OsdMode showMode = OsdMode.Auto, bool dontShow = false)
```

##### Parameters

- *text*  (`string`):
    Text in OSD window.
Sets `Au.osdText.Text`.
- *secondsTimeout*  (`int`):
    Close the OSD window after this time, seconds. If 0 (default), depends on text length. Can be `System.Threading.Timeout.Infinite` (-1). Sets `Au.osdText.SecondsTimeout`.
- *xy*  (`Au.Types.PopupXY`):
    Coordinates. Default: `null` (screen center). Sets `Au.osdText.XY`.
- *icon*  (`object`):
    Icon or image at the left. Any size. Sets `Au.osdText.Icon`.
- *textColor*  (`Au.Types.ColorInt?`):
    Text color. Default: `Au.osdText.defaultTextColor`. Sets `Au.osdText.TextColor`.
- *backColor*  (`Au.Types.ColorInt?`):
    Background color. Default: `Au.osdText.defaultBackColor`. Sets `Au.osdText.BackColor`.
- *font*  (`Au.Types.FontNSS`):
    Font. Default: `Au.osdText.defaultSmallFont`. Sets `Au.osdText.Font`.
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

Also sets these properties: `Au.osdText.ClickToClose`=`true`, `Au.osdText.Shadow`=`true`.