# Enum `Au.Types.EFFlags`

Flags for "find UI element" functions (`Au.elmFinder`).

```
[Flags]
public enum EFFlags
```

### Fields

| Name | Description |
| --- | --- |
| ClientArea | Search only in the client area of the window or control. Skips the title bar, standard menubars and scrollbars. Searches only in the client area root UI element (but will not find the UI element itself). When control class or id is specified in the *prop* argument, this flag is applied to these controls. Not applied to other controls. Don't use this flag when searching in elm or web page (role prefix `"web:"` etc) or with flag `UIA`. |
| HiddenToo | The UI element can be invisible. Without this flag skips UI elements that are invisible (have state `INVISIBLE`) or are descendants of invisible `WINDOW`, `DOCUMENT`, `PROPERTYPAGE`, `GROUPING`, `ALERT`, `MENUPOPUP`. Regardless of this flag, always skips invisible standard UI elements of nonclient area: `TITLEBAR`, `MENUBAR`, `SCROLLBAR`, `GRIP`. |
| MenuToo | Always search in `MENUITEM`. Without this flag skips `MENUITEM` descendant elements (for speed), unless *role* argument is `MENUITEM` or `MENUPOPUP` or searching in web page. |
| NotInProc | Search without loading dll into the target process. Disadvantages: 1. Much slower. 2. Some properties are not supported, for example HTML attributes (while searching and later). 3. And more. Even without this flag, the default search method is not used with Windows Store app windows, console windows, most Java windows, windows of protected processes and processes of higher [UAC](../articles/UAC.html) integrity level. Some windows have child controls that belong to a different process or thread than the window. For example the Windows Task Scheduler window. When searching in such windows, the default search method is not used when searching in these controls. Workaround - find the control (`Au.wnd.Child` etc) and search in it. Don't need this flag when searching in elm (then it is inherited from the elm variable). See also: `Au.elm.MiscFlags`. |
| Reverse | Search in reverse order. It can make faster. When control class or id is specified in the *prop* argument, controls are searched not in reverse order. Only UI elements in them are searched in reverse order. |
| UIA | Use UI Automation API. Need this flag to find UI elements in windows that don't support accessible objects but support UI Automation elements. UI elements found with this flag never have `HtmlX` properties, but can have `UiaX` properties. This flag can be used with most other windows too. Don't use this flag when searching in elm (then it is inherited from the elm variable) or web page (role prefix `"web:"` etc). See also: `Au.elm.MiscFlags`. |