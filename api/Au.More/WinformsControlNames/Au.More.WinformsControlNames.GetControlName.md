# Method `Au.More.WinformsControlNames.GetControlName`

Gets control name.

```
public string GetControlName(wnd c)
```

##### Parameters

- *c*  (`Au.wnd`):
    The control. Can be a top-level window too. Must be of the same process as the window specified in the constructor.

##### Returns

`string`

`null` if failed or the name is empty.