# Method `Au.wnd.getwnd.allWindows`

Gets top-level windows.

```
public static wnd[] allWindows(bool onlyVisible = false, bool sortFirstVisible = false)
```

##### Parameters

- *onlyVisible*  (`bool`):
    Need only visible windows. Note: this function does not check whether windows are cloaked, as it is rather slow. Use `Au.wnd.IsCloaked` if need.
- *sortFirstVisible*  (`bool`):
    Place hidden windows at the end of the array. Not used when *onlyVisible* is `true`.

##### Returns

`Au.wnd[]`

Array containing zero or more `Au.wnd`.

#### Remarks

Calls API `EnumWindows`. Although undocumented, the API retrieves most windows as in the Z order, however places IME windows (hidden) at the end. See also: `Au.wnd.getwnd.allWindowsZorder`;

> **Note:**
> The array can be bigger than you expect, because there are many invisible windows, tooltips, etc. See also `Au.wnd.getwnd.mainWindows`.

Skips message-only windows; use `Au.wnd.findFast` if need. On Windows 8 and later may skip Windows Store app Metro-style windows (on Windows 10 few such windows exist). It happens if this program does not have `disableWindowFiltering = true` in its manifest and is not uiAccess; to find such windows you can use `Au.wnd.findFast`. Tip: To get top-level and child windows in single array: `var a = wnd.getwnd.root.Get.Children();`.

### See Also

`Au.wnd.getwnd.Children`

`Au.wnd.findAll`