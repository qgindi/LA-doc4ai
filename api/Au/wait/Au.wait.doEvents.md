# Method `Au.wait.doEvents`

## Overload 1

Waits *timeMS* milliseconds. While waiting, retrieves and dispatches Windows messages and other events.

```
public static void doEvents(int timeMS)
```

##### Parameters

- *timeMS*  (`int`):
    Time to wait, milliseconds. Or `System.Threading.Timeout.Infinite` (-1).

##### Exceptions

- `ArgumentOutOfRangeException`:
    *timeMS* is negative and not -1 (`Timeout.Infinite`).

#### Remarks

Unlike `Au.wait.ms`, this function retrieves and dispatches Windows messages, calls .NET event handlers, hook procedures, timer functions, COM, etc. This function can be used in threads with windows. However usually there are better ways, for example timer, other thread, `async`/`await`/`Task`. If *timeMS* is -1, returns when receives `WM_QUIT` message.

* * *

## Overload 2

Retrieves and dispatches events and Windows messages from the message queue of this thread.

```
public static bool doEvents()
```

##### Returns

`bool`

`false` if received `WM_QUIT` message.

#### Remarks

Similar to `System.Windows.Forms.Application.DoEvents`, but more lightweight. Uses API functions `PeekMessage`, `TranslateMessage` and `DispatchMessage`.