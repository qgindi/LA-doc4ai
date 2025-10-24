# Method `Au.More.WndUtil.SetOwnerWindow`

Changes the owner window.

```
public static bool SetOwnerWindow(wnd w, wnd owner)
```

##### Parameters

- *w*  (`Au.wnd`)
- *owner*  (`Au.wnd`)

##### Returns

`bool`

If fails, returns `false`; supports `Au.lastError`.

#### Remarks

A window that has an owner window is always on top of it. Don't call this for controls, they don't have an owner window. Fails for example if the owner's process has higher [UAC](../articles/UAC.html) integrity level or is a Store app.

### See Also

`Au.wnd.getwnd.Owner`