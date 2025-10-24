# Enum `Au.Types.EObjid`

Object ids of window parts and some special UI elements. Used with `Au.elm.fromWindow`

```
public enum EObjid
```

##### Remarks

Most names are as in API `AccessibleObjectFromWindow` documentation but without prefix `OBJID_`.

### Fields

| Name | Description |
| --- | --- |
| ALERT |  |
| CARET |  |
| CLIENT |  |
| CURSOR |  |
| HSCROLL |  |
| Java | The root Java UI element. Can be used when the window's class name starts with `"SunAwt"`. |
| MENU |  |
| NATIVEOM | Not used with `Au.elm.fromWindow`. |
| QUERYCLASSNAMEIDX | Not used with `Au.elm.fromWindow`. |
| SIZEGRIP |  |
| SOUND |  |
| SYSMENU |  |
| TITLEBAR |  |
| UIA | Use UI Automation API. More info: `Au.Types.EFFlags.UIA`. |
| UiaRootObjectId | Not used with `Au.elm.fromWindow`. |
| VSCROLL |  |
| WINDOW |  |