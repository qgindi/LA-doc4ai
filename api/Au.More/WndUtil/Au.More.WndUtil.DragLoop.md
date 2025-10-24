# Method `Au.More.WndUtil.DragLoop`

Simple non-OLE drag operation.

```
public static bool DragLoop(AnyWnd window, MButtons mouseButton = MButtons.Left, Action<WDLArgs> onMouseKeyMessage = null)
```

##### Parameters

- *window*  (`Au.Types.AnyWnd`):
    Window or control that owns the drag operation. Must be of this thread.
- *mouseButton*  (`Au.Types.MButtons`):
    Mouse button that is used for the drag operation: `Left`, `Right`, `Middle`.
- *onMouseKeyMessage*  (`Action<Au.Types.WDLArgs>`):
    Callback function, called on each received mouse/key message. Optional.

##### Returns

`bool`

`true` if dropped, `false` if canceled.