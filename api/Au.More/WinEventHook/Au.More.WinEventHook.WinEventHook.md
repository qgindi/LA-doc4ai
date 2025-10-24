# Constructor of `Au.More.WinEventHook`

## Overload 1

Sets a hook for an event or a range of events.

```
public WinEventHook(EEvent eventMin, EEvent eventMax, Action<HookData.WinEvent> hookProc, int idProcess = 0, int idThread = 0, EHookFlags flags = EHookFlags.None)
```

##### Parameters

- *eventMin*  (`Au.Types.EEvent`):
    The lowest event constant value in the range of events. Can be `Au.Types.EEvent.MIN` to indicate the lowest possible event value. Events reference: `SetWinEventHook`. Value 0 is ignored.
- *eventMax*  (`Au.Types.EEvent`):
    The highest event constant value in the range of events. Can be `Au.Types.EEvent.MAX` to indicate the highest possible event value. If 0, uses *eventMin*.
- *hookProc*  (`Action<Au.Types.HookData.Au.Types.HookData.WinEvent>`):
    The hook procedure (function that handles hook events).
- *idProcess*  (`int`):
    The id of the process from which the hook function receives events. If 0 - all processes on the current desktop.
- *idThread*  (`int`):
    The native id of the thread from which the hook function receives events. If 0 - all threads.
- *flags*  (`Au.Types.EHookFlags`)

##### Exceptions

- `Au.Types.AuException`:
    Failed.

#### Examples

See `Au.More.WinEventHook`.

* * *

## Overload 2

Sets multiple hooks.

```
public WinEventHook(EEvent[] events, Action<HookData.WinEvent> hookProc, int idProcess = 0, int idThread = 0, EHookFlags flags = EHookFlags.None)
```

##### Parameters

- *events*  (`Au.Types.EEvent[]`):
    Events. Reference: API `SetWinEventHook`. Elements with value 0 are ignored.
- *hookProc*  (`Action<Au.Types.HookData.Au.Types.HookData.WinEvent>`):
    The hook procedure (function that handles hook events).
- *idProcess*  (`int`):
    The id of the process from which the hook function receives events. If 0 - all processes on the current desktop.
- *idThread*  (`int`):
    The native id of the thread from which the hook function receives events. If 0 - all threads.
- *flags*  (`Au.Types.EHookFlags`)

##### Exceptions

- `Au.Types.AuException`:
    Failed.

#### Examples

See `Au.More.WinEventHook`.