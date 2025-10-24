# Method `Au.More.WndUtil.DestroyWindow`

Destroys a native window of this thread. Calls API `DestroyWindow`.

```
public static bool DestroyWindow(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`)

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

### See Also

`Au.wnd.Close`