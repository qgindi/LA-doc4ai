# Method `Au.timer2.after`

Creates and starts new one-time timer.

```
public static timer2 after(long milliseconds, Action<timer2> timerAction, object tag = null)
```

##### Parameters

- *milliseconds*  (`long`):
    Time interval after which to call the callback function. Valid values are 0 - `System.UInt32.MaxValue` - 2. If -1, stops without disposing.
- *timerAction*  (`Action<Au.timer2>`):
    Callback function.
- *tag*  (`object`):
    Something to pass to the callback function as `Au.timer2.Tag`.

##### Returns

`Au.timer2`

##### Exceptions

- `ArgumentOutOfRangeException`

#### Remarks

Calls `System.Threading.Timer.Change`.