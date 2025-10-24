# Method `Au.Triggers.WindowTriggers.LogEvents`

Starts or stops to log (write in output) window events that can help to create or debug window triggers.

```
public void LogEvents(bool on, Func<wnd, bool> skip = null)
```

##### Parameters

- *on*  (`bool`):
    Start (`true`) or stop.
- *skip*  (`Func<Au.wnd, bool>`):
    An optional callback function that can be used to reduce noise, eg skip tooltip windows. Return `true` to skip that window.

#### Remarks

For primary trigger events is logged this info:

1. Time milliseconds. Shows only the remainder of dividing by 10 seconds, therefore it starts from 0 again when reached 9999 (9 seconds and 999 milliseconds).
2. Event (see `Au.Triggers.TWLater`).
3. Letters for window state etc:
    - `A` - the window is active.
    - `H` - the window is invisible (!`Au.wnd.IsVisible`).
    - `C` - the window is cloaked (`Au.wnd.IsCloaked`).
    - `O` - the window is considered old, ie created before calling `Au.Triggers.ActionTriggers.Run`.
    - `T` - the even has been detected using a timer, which means slower response time. Else detected using a hook.
4. Window (handle, class, name, program, rectangle).

Colors are used for window event types used for primary triggers: blue if activated; green if became visible; yellow if name changed. For "later" events is logged time, event and window. Black, tab-indented. Only events that are specified in triggers. When a trigger is activated, the event type is red.

#### Examples

```
Triggers.Window.LogEvents(true, o => 0 != o.ClassNameIs("*tooltip*", "SysShadow", "#32774", "TaskList*"));
```