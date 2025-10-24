# Method `Au.osdText.showImage`

Shows on-screen image.

```
public static osdText showImage(Image image, int secondsTimeout = 0, PopupXY xy = null, string name = null, OsdMode showMode = OsdMode.Auto, bool dontShow = false)
```

##### Parameters

- *image*  (`Image`):
    Sets `Au.osdText.BackgroundImage`.
- *secondsTimeout*  (`int`):
    Close the OSD window after this time, seconds. If 0 (default), depends on text length. Can be `System.Threading.Timeout.Infinite` (-1). Sets `Au.osdText.SecondsTimeout`.
- *xy*  (`Au.Types.PopupXY`):
    Coordinates. Default: `null` (screen center). Sets `Au.osdText.XY`.
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

Also sets these properties: `Au.osdText.IsOfImageSize`=`true`, `Au.Types.OsdWindow.Opacity`=0, `Au.osdText.ClickToClose`=`true`.