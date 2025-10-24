# Method `Au.More.WinEventHook.Add`

Adds a hook for an event or a range of events.

```
public int Add(EEvent eventMin, EEvent eventMax = 0, int idProcess = 0, int idThread = 0, EHookFlags flags = EHookFlags.None)
```

##### Parameters

- *eventMin*  (`Au.Types.EEvent`):
    The lowest event constant value in the range of events. Can be `Au.Types.EEvent.MIN` to indicate the lowest possible event value. Events reference: `SetWinEventHook`. Value 0 is ignored.
- *eventMax*  (`Au.Types.EEvent`):
    The highest event constant value in the range of events. Can be `Au.Types.EEvent.MAX` to indicate the highest possible event value. If 0, uses *eventMin*.
- *idProcess*  (`int`):
    The id of the process from which the hook function receives events. If 0 - all processes on the current desktop.
- *idThread*  (`int`):
    The native id of the thread from which the hook function receives events. If 0 - all threads.
- *flags*  (`Au.Types.EHookFlags`)

##### Returns

`int`

An `int` value greater than 0 that can be used with `Au.More.WinEventHook.Remove`.

##### Exceptions

- `Au.Types.AuException`:
    Failed.

#### Remarks

Parameters are the same as of the constructor, but values can be different.

This function together with `Au.More.WinEventHook.Remove` can be used to temporarily add/remove one or more hooks while using the same `Au.More.WinEventHook` variable and hook procedure. Don't need to call `Au.More.WinEventHook.Unhook` before.

#### Examples

See `Au.More.WinEventHook`.