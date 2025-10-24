# Method `Au.timer.after`

Creates and starts new one-time timer.

```
public static timer after(int milliseconds, Action<timer> timerAction, object tag = null)
```

##### Parameters

- *milliseconds*  (`int`):
    Time interval after which to call the callback function. The actual minimal interval is 10-20 ms.
- *timerAction*  (`Action<Au.timer>`):
    Callback function.
- *tag*  (`object`):
    Something to pass to the callback function as `Au.timer.Tag`.

##### Returns

`Au.timer`

New `Au.timer` object. Usually you don't need it.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Negative.
- `Win32Exception`:
    API `SetTimer` returned 0. Unlikely.

#### Remarks

The timer will be stopped before calling the callback function. The callback function can start it again. The callback function will be called in this thread. This thread must get/dispatch posted messages, eg call `Application.Run` or `Au.dialog.show`. The callback function is not called while this thread does not do it.