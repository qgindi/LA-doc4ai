# Method `Au.elm.fromEvent`

Gets the UI element that generated the event that is currently being processed by the callback function used with API `SetWinEventHook` or `Au.More.WinEventHook`.

```
public static elm fromEvent(wnd w, EObjid idObject, int idChild)
```

##### Parameters

- *w*  (`Au.wnd`)
- *idObject*  (`Au.Types.EObjid`)
- *idChild*  (`int`)

##### Returns

`Au.elm`

`null` if failed. Supports `Au.lastError`.

#### Remarks

The parameters are of the callback function. Uses API `AccessibleObjectFromEvent`. Often fails because the UI element already does not exist, because the callback function is called asynchronously, especially when the event is `OBJECT_DESTROY`, `OBJECT_HIDE`, `SYSTEM_xEND`. Returns `null` if failed. Always check the return value, to avoid `System.NullReferenceException`. An exception in the callback function kills this process.