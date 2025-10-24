# Method `Au.miscInfo.getGUIThreadInfo`

Calls API `GetGUIThreadInfo`. It gets info about mouse capturing, menu mode, move/size mode, focus, caret, etc.

```
public static bool getGUIThreadInfo(out GUITHREADINFO g, int idThread = 0)
```

##### Parameters

- *g*  (`Au.Types.GUITHREADINFO`):
    API `GUITHREADINFO`.
- *idThread*  (`int`):
    Thread id. If 0 - the foreground (active window) thread. See `Au.process.thisThreadId`, `Au.wnd.ThreadId`.

##### Returns

`bool`