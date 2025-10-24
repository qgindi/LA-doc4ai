# Enum `Au.Types.WXYFlags`

Flags for `Au.wnd.fromXY` and `Au.wnd.fromMouse`.

```
[Flags]
public enum WXYFlags
```

### Fields

| Name | Description |
| --- | --- |
| NeedControl | Need a control (child window). Returns `default(wnd)` if there is no control at that point. Don't use together with `NeedWindow`. Without flags `NeedWindow` and `NeedControl` the function gets control or top-level window. |
| NeedWindow | Need top-level window. If at that point is a control, gets its top-level parent. Don't use together with `NeedControl`. |
| Raw | Just call API `WindowFromPhysicalPoint`. Faster, but skips disabled controls and in some cases gets transparent control like group box although a smaller visible sibling is there. Not used with flag `NeedWindow`. |