# Method `Au.timer2.every`

Creates and starts new periodic timer.

```
public static timer2 every(long milliseconds, Action<timer2> timerAction, object tag = null, long? firstAfter = null)
```

##### Parameters

- *milliseconds*  (`long`):
    Time interval (period) of calling the callback function. Valid values are 0 - `System.UInt32.MaxValue` - 2.
- *timerAction*  (`Action<Au.timer2>`):
    Callback function.
- *tag*  (`object`):
    Something to pass to the callback function as `Au.timer2.Tag`.
- *firstAfter*  (`long?`):
    `null` (default) or time interval after which to call the callback function first time. Valid values are 0 - `System.UInt32.MaxValue` - 2.

##### Returns

`Au.timer2`

##### Exceptions

- `ArgumentOutOfRangeException`

#### Remarks

Calls `System.Threading.Timer.Change`.