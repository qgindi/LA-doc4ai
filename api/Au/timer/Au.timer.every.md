# Method `Au.timer.every`

Creates and starts new periodic timer.

```
public static timer every(int milliseconds, Action<timer> timerAction, object tag = null)
```

##### Parameters

- *milliseconds*  (`int`):
    Time interval (period) of calling the callback function. The actual minimal period is 10-20 ms.
- *timerAction*  (`Action<Au.timer>`):
    Callback function.
- *tag*  (`object`):
    Something to pass to the callback function as `Au.timer.Tag`.

##### Returns

`Au.timer`

New `Au.timer` object that can be used to modify timer properties if you want to do it not in the callback function; usually don't need it.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Negative.
- `Win32Exception`:
    API `SetTimer` returned 0. Unlikely.

#### Remarks

The callback function can stop the timer or restart with different period. The callback function will be called in this thread. This thread must get/dispatch posted messages, eg call `Application.Run` or `Au.dialog.show`. The callback function is not called while this thread does not do it.