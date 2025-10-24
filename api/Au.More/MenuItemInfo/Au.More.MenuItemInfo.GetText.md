# Method `Au.More.MenuItemInfo.GetText`

## Overload 1

Gets menu item text.

```
public string GetText(bool removeHotkey, bool removeAmp)
```

##### Parameters

- *removeHotkey*  (`bool`):
    If contains `'\t'` character, get substring before it.
- *removeAmp*  (`bool`):
    Call `Au.More.StringUtil.RemoveUnderlineChar`.

##### Returns

`string`

`null` if failed.

* * *

## Overload 2

Gets menu item text.

```
public static string GetText(nint menuHandle, int id, bool byIndex, bool removeHotkey, bool removeAmp)
```

##### Parameters

- *menuHandle*  (`nint`)
- *id*  (`int`)
- *byIndex*  (`bool`):
    id is 0-based index. For example you can use it to get text of a submenu-item, because such items usually don't have id.
- *removeHotkey*  (`bool`):
    If contains `'\t'` character, get substring before it.
- *removeAmp*  (`bool`):
    Call `Au.More.StringUtil.RemoveUnderlineChar`.

##### Returns

`string`

`null` if failed.