# Method `Au.elm.ScrollTo`

Scrolls this UI element into view.

```
public void ScrollTo()
```

##### Exceptions

- `Au.Types.AuException`:
    Failed to scroll, or the UI element does not support scrolling.

#### Remarks

This function works with these UI elements:

- Web page elements in Chrome, Internet Explorer and apps that use their code (Edge, Opera, web browser controls...). To find UI element, use role prefix `"web:"`, `"firefox:"` or `"chrome:"`, and don't use flag `Au.Types.EFFlags.NotInProc`.
- Standard treeview, listview and listbox controls.
- Some other controls if found with flag `Au.Types.EFFlags.UIA`.

Some apps after scrolling update `Au.elm.Rect` with a delay. Some apps never update it for existing `Au.elm` variables. This function does not wait.