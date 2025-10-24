# Method `Au.wnd.GetText`

Gets window/control name or control text. This is a low-level function. You can instead use `Au.wnd.Name` and `Au.wnd.ControlText`.

```
public string GetText(bool? getText = null, bool removeUnderlineAmpersand = true)
```

##### Parameters

- *getText*  (`bool?`):

    How to get text:

    - `false` - use API `InternalGetWindowText`. This is used by `Au.wnd.Name`.
    - `true` - use API `WM_GETTEXT`. It is slow and prefers editable text. This is used by `Au.wnd.ControlText`. Fails if the window is hung.
    - `null` - try `InternalGetWindowText`. If it gets `""` and this is a control, then try `WM_GETTEXT`.
- *removeUnderlineAmpersand*  (`bool`):
    Remove the invisible `'&'` characters that are used to underline keyboard shortcuts with the `Alt` key. Removes only if this is a control (has style `Au.Types.WS.CHILD`). Calls `Au.More.StringUtil.RemoveUnderlineChar`.

##### Returns

`string`

Returns `""` if no text. Returns `null` if failed, eg if the window is closed. Supports `Au.lastError`.

### See Also

`Au.wnd.SetText`

`Au.wnd.NameElm`

`Au.wnd.NameWinforms`