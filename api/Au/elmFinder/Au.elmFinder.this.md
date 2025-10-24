# Indexer of `Au.elmFinder`

Creates an `Au.elmFinder` for finding a UI element. Supports path like `var e = w.Elm["ROLE1", "Name1"]["ROLE2", "Name2"].Find();`.

```
public elmFinder this[string role = null, string name = null, Strings prop = default, EFFlags flags = 0, Func<elm, bool> also = null, int skip = 0, string navig = null] { get; }
```

##### Parameters

- *role*  (`string`):
    UI element role (`Au.elm.Role`), like `"LINK"`. Can have prefix `"web:"`, `"firefox:"` or `"chrome:"` which means "search only in web page" and enables Chrome UI elements. Case-sensitive. Not wildcard. `null` means "can be any". Cannot be `""`. More info in Remarks.
- *name*  (`string`):
    UI element name (`Au.elm.Name`). String format: [wildcard expression](../articles/Wildcard%20expression.html). `null` means "any". `""` means "empty or unavailable".
- *prop*  (`Au.Types.Strings`):
    Other UI element properties and search settings. Examples: `"value=xxx|@href=yyy"`, `new("value=xxx", "@href=yyy")`. More info in Remarks.
- *flags*  (`Au.Types.EFFlags`)
- *also*  (`Func<Au.elm, bool>`):
    Callback function. Called for each matching UI element. Let it return `true` if this is the wanted UI element. Example: the UI element must contain point x y: `o => o.GetRect(out var r, o.WndTopLevel) && r.Contains(266, 33)`
- *skip*  (`int`):
    0-based index of matching UI element to use. Will skip this number of matching elements. Value -1 means "any", and can be useful when this finder is intermediate (ie not the last) in a path or when it has *navig*. If intermediate, will search for next element in all matching intermediate elements. If has *navig*, will retry with other matching elements if fails to navigate in the first found. It is slower and not so often useful, therefore the default value of this parameter is 0, not -1. Cannot be used with `Au.elmFinder.FindAll`, unless it is not in the last part of path.
- *navig*  (`string`):
    If not `null`, after finding the specified UI element will call `Au.elm.Navigate` with this string and use its result instead of the found element.

##### Exceptions

- `ArgumentException`:
    *flags* contains `UIA` or `ClientArea` when appending (only the first finder can have these flags).

##### Property Value

`Au.elmFinder`

The new finder or the first finder in path.

#### Remarks

To create code for this function, use tool **Find UI element**.

In [wildcard expression](../articles/Wildcard%20expression.html) supports PCRE regular expressions (prefix `"**r "`) but not .NET regular expressions (prefix `"**R "`). They are similar.

When using path like `["ROLE1", "Name1"]["ROLE2", "Name2"]["ROLE3", "Name3"]`, multiple finders are linked like finder1 -> finder2 -> finder3, so that the chain of finders will find UI element specified by the last finder.

More info in `Au.elm` topic.

##### About the *role* parameter

Can be standard role (see `Au.Types.ERole`) like `"LINK"` or custom role like `"div"`. See `Au.elm.Role`.

Can have a prefix:

- `"web:"` - search only in the visible web page, not in whole window. Example: `"web:LINK"`.
 Supports Chrome, Firefox, Internet Explorer (IE) and apps that use same code (Edge, Opera...). With other windows, searches in the first found visible UI element that has `DOCUMENT` role.
 Tip: To search only NOT in web pages, use *prop* `"notin=DOCUMENT"` (Chrome, Firefox) or `"notin=PANE"` (IE).
- `"firefox:"` - search only in the visible web page of Firefox or Firefox-based web browser. If *w* window class name starts with `"Mozilla"`, can be used `"web:"` instead.
- `"chrome:"` - search only in the visible web page of Chrome or Chrome-based web browser. If *w* window class name starts with `"Chrome"`, can be used `"web:"` instead.

> **Note:**
> Chrome web page UI elements normally are disabled (don't exist). Use prefix `"web:"` or `"chrome:"` to enable.

Prefix cannot be used:

- if *prop* contains `"id"` or `"class"`;
- with flags `UIA`, `ClientArea`;
- when searching in `Au.elm`.

##### About the *prop* parameter

Format: one or more `"name=value"` strings, like `new("key=xxx", "@href=yyy")` or `"key=xxx|@href=yyy"`. Names must match case. Values of most string properties are [wildcard expressions](../articles/Wildcard%20expression.html).

- `"class"` - search only in child controls that have this class name (see `Au.wnd.ClassName`).
 Cannot be used when searching in a UI element.
- `"id"` - search only in child controls that have this id (see `Au.wnd.ControlId`). If the value is not a number - Windows Forms control name (see `Au.wnd.NameWinforms`); case-sensitive, not wildcard.
 Cannot be used when searching in a UI element.
- `"value"` - `Au.elm.Value`.
- `"desc"` - `Au.elm.Description`.
- `"state"` - `Au.elm.State`. List of states the UI element must have and/or not have.
 Example: `"state=CHECKED, FOCUSABLE, !DISABLED"`.
 Example: `"state=0x100010, !0x1"`.
 Will find UI element that has all states without `"!"` prefix and does not have any of states with `"!"` prefix.
- `"rect"` - `Au.elm.GetRect` with *raw* `true`. Can be specified left, top, width and/or height, using `Au.Types.RECT.ToString` format.
 Example: `"rect={L=1155 T=1182 W=132 H=13}"`. Example: `"rect={W=132 T=1182}"`. The `L T` coordinates are relative to the primary screen.
- `"level"` - level (see `Au.elm.Level`) at which the UI element can be found. Can be exact level, or minimal and maximal level separated by space.
 The default value is 0 1000.
- `"item"` - `Au.elm.Item`.
- `"action"` - `Au.elm.DefaultAction`.
- `"key"` - `Au.elm.KeyboardShortcut`.
- `"help"` - `Au.elm.Help`.
- `"uiaid"` - `Au.elm.UiaId`.
- `"uiacn"` - `Au.elm.UiaCN`.
- `"url"` - URL of the container DOCUMENT in Chromium-based web browser. Used together with role prefix `"web:"` or `"chrome:"`. Use when the document is a side panel or developer tools or a special page like Settings. Don't need (but can be used too) when the document is a web page (URL starts with `"https:"`, `"http:"` or `"file:"`).
- `"maxcc"` - when searching, skip children of UI elements that have more than this number of direct children. Default 10000, min 1, max 1000000.
 It can make faster. It also prevents hanging or crashing when a UI element in the UI element tree has large number of children. For example OpenOffice Calc `TABLE` has one billion children.
- `"notin"` - when searching, skip children of UI elements that have these roles. It can make faster.
 Example: `"notin=TREE,LIST,TOOLBAR"`.
 Roles in the list must be separated with `","` or `", "`. Case-sensitive, not wildcard. See also: `Au.Types.EFFlags.MenuToo`.
- `"@attr"` - `Au.elm.HtmlAttribute`. Here `"attr"` is any attribute name. Example: `"@href=example"`.

### See Also

`Au.elm.path`

`Au.elmFinder.Next`