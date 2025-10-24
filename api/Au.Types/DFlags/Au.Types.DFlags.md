# Enum `Au.Types.DFlags`

Flags for `Au.dialog` functions.

```
[Flags]
public enum DFlags
```

### Fields

| Name | Description |
| --- | --- |
| CenterMouse | Show the dialog at the mouse position. |
| CenterOwner | Show the dialog in the center of the owner window. |
| CommandLinks | Display custom buttons as a column of command-links, not as a row of classic buttons. Command links can have multi-line text. The first line has bigger font. More info about custom buttons: `Au.dialog.Buttons`. |
| ExpandDown | Show expanded text in footer. |
| MinimizeButton | Add **Minimize** button to the title bar. This flag is ignored if owner window specified. |
| NoTopmost | Don't make the dialog a topmost window, regardless of `Au.dialog.options.topmostIfNoOwnerWindow` etc. |
| RawXY | x y are raw coordinates relative to the primary screen. More info: `Au.dialog.XY`, `Au.dialog.InScreen`. |
| Topmost | (see section `details1` in Footnotes) |
| Wider | Call `Au.dialog.Wider` with *width* 700. |
| XCancel | Allow to cancel even if there is no **Cancel** button. It adds **X** (Close) button to the title bar, and also allows to close the dialog with the `Esc` key. When the dialog is closed with the **X** button or `Esc`, the returned result button id is 0 if there is no `Cancel` button; else the same as when clicked the `Cancel` button. |

## Footnotes

###### details1

Make the dialog a topmost window (always on top of other windows), regardless of `Au.dialog.options.topmostIfNoOwnerWindow` etc.

If neither `Topmost` nor `NoTopmost` are set, makes topmost if both these are true: no owner window, `Au.dialog.options.topmostIfNoOwnerWindow` is `true` (default).