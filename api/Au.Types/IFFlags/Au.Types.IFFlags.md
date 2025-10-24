# Enum `Au.Types.IFFlags`

Flags for `Au.uiimage.find` and similar functions.

```
[Flags]
public enum IFFlags
```

### Fields

| Name | Description |
| --- | --- |
| Parallel | This flag can make the function faster when *image* is a list of images. To search for each image, the function will use `System.Threading.Tasks.Parallel.For` instead of `for`. For example, if the CPU has 4 cores (8 threads), can search for max 8 images simultaneously. However it does not mean it will be 8 times faster. Can be max 2 or 3 times faster, depending on the number of images, flag `WindowDC`, *diff*, *also*, CPU, RAM, area size, finds or not, image position, etc. Can be even slower. To measure speed, use `Au.perf`. If used *also* callback function, it runs in any thread and any order, but one at a time (inside `lock() { }`). |
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