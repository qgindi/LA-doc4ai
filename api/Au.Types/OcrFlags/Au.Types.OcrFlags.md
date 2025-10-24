# Enum `Au.Types.OcrFlags`

Flags for `Au.ocr` and `Au.ocrFinder`.

```
[Flags]
public enum OcrFlags
```

### Fields

| Name | Description |
| --- | --- |
| PrintWindow | (see section `details1` in Footnotes) |
| WindowDC | Get pixels from the device context (DC) of the window client area, not from screen DC. Usually much faster. Can get pixels from window parts that are covered by other windows or offscreen. But not from hidden and minimized windows. Does not work on Windows 7 if Aero theme is turned off. Then this flag is ignored. Cannot find images in some windows (including Windows Store apps), and in some window parts (glass). All pixels captured from these windows/parts are black. If the window is partially or completely transparent, the image must be captured from its non-transparent version. If the window is DPI-scaled, the image must be captured from its non-scaled version. However if used a limiting rectangle, it must contain scaled coordinates. |

## Footnotes

###### details1

Use API `PrintWindow` to get window pixels. Like `WindowDC`, works with background windows, etc. Differences:

- On Windows 8.1 and later works with windows where `WindowDC` doesn't.
- Works without Aero theme too.
- Slower.
- Some windows flicker.
- From some controls randomly gets partial image (API bug).
- Does not work with windows of higher [UAC](../articles/UAC.html) integrity level (throws exception).
- Unreliable with DPI-scaled windows; the window image slightly changes when resizing etc.