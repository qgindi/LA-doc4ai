# Enum `Au.Types.PMFlags`

Flags for `Au.popupMenu` `ShowX` methods.

```
[Flags]
public enum PMFlags
```

##### Remarks

The `AlignX` flags are for API `TrackPopupMenuEx`.

### Fields

| Name | Description |
| --- | --- |
| AlignBottom | Vertically align the menu so that the show position would be at its bottom. |
| AlignCenterH | Horizontally align the menu so that the show position would be in its center. |
| AlignCenterV | Vertically align the menu so that the show position would be in its center. |
| AlignRectBottomTop | Show at the bottom or top of *excludeRect*, not at the right/left. |
| AlignRight | Horizontally align the menu so that the show position would be at its right side. |
| ByCaret | Show by the caret (text cursor) position. If not possible, use flag `WindowCenter` or `ScreenCenter` or *xy* or mouse position. |
| ScreenCenter | Show in the center of the screen that contains the mouse pointer. |
| Underline | Underline characters preceded by `&`, regardless of Windows settings. More info: `Au.More.StringUtil.RemoveUnderlineChar`. |
| WindowCenter | Show in the center of the active window. |