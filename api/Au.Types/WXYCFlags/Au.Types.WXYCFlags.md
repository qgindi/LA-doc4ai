# Enum `Au.Types.WXYCFlags`

Flags for `Au.wnd.ChildFromXY`.

```
[Flags]
public enum WXYCFlags
```

### Fields

| Name | Description |
| --- | --- |
| DirectChild | Must be direct child of this. Default - any descendant. |
| Inside | If the point is not in client area, don't look for descendants; if with flag `OrThis` and the point is in this (non-client area), return this, else return `default(wnd)`. |
| OrThis | If the point is in this window but not in a descendant control, return this. Default - return `default(wnd)`. |
| ScreenXY | The point is in screen coordinates. Default - client area. |