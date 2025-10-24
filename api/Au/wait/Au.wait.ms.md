# Method `Au.wait.ms`

Waits *timeMilliseconds* milliseconds.

```
public static void ms(this int timeMilliseconds)
```

##### Parameters

- *timeMilliseconds*  (`int`):
    Time to wait, milliseconds. Or `System.Threading.Timeout.Infinite` (-1).

##### Exceptions

- `ArgumentOutOfRangeException`:
    *timeMilliseconds* is negative and not -1 (`Timeout.Infinite`).

#### Remarks

Calls `System.Threading.Thread.Sleep`. Does not process Windows messages and other events, therefore should not be used in threads with windows, timers, hooks, events or COM, unless *timeMilliseconds* is small. Supports APC. If the computer goes to sleep or hibernate during that time, the real time is the specified time + the sleep/hibernate time.

Tip: the script editor replaces code like `100ms` with `100.ms();` when typing.

#### Examples

```
wait.ms(500);
500.ms(); //the same (ms is an extension method)
wait.s(0.5); //the same
```