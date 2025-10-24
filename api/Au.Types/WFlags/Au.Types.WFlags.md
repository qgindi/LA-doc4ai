# Enum `Au.Types.WFlags`

Flags of `Au.wnd.find` and similar functions.

```
[Flags]
public enum WFlags
```

### Fields

| Name | Description |
| --- | --- |
| CloakedToo | Can find cloaked windows. See `Au.wnd.IsCloaked`. Cloaked are windows hidden not in the classic way, therefore `Au.wnd.IsVisible` does not detect it, but `Au.wnd.IsCloaked` detects. For example, windows on inactive Windows 10 virtual desktops, ghost windows of inactive Windows Store apps, various hidden system windows. Use this carefully. Always use *cn* (class name), not just *name*, to avoid finding a wrong window with the same name. |
| HiddenToo | Can find invisible windows. See `Au.wnd.IsVisible`. Use this carefully. Always use *cn* (class name), not just *name*, to avoid finding a wrong window with the same name. |