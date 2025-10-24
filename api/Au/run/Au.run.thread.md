# Method `Au.run.thread`

## Overload 1

Starts new thread: creates new `System.Threading.Thread` object, sets some properties and calls `System.Threading.Thread.Start`.

```
public static Thread thread(Action threadProc, bool background = true, bool sta = true)
```

##### Parameters

- *threadProc*  (`Action`):
    Thread procedure. Parameter *start* of `System.Threading.Thread` constructor.
- *background*  (`bool`):
    If `true` (default), sets `System.Threading.Thread.IsBackground` = `true`. The process ends when the main thread and all foreground threads end; background threads then are terminated.
- *sta*  (`bool`):
    If `true` (default), sets `System.Threading.ApartmentState.STA`.

##### Returns

`Thread`

The `Thread` variable.

##### Exceptions

- `OutOfMemoryException`

* * *

## Overload 2

Starts new thread like `Au.run.thread(Action, bool, bool)` and gets thread handle and native id.

```
public static SafeWaitHandle thread(out int id, out Thread thread, Action threadProc, bool background = true, bool sta = true, Action init = null)
```

##### Parameters

- *id*  (`int`):
    Native thread id.
- *thread*  (`Thread`):
    `Thread` object.
- *threadProc*  (`Action`):
    Thread procedure. Parameter *start* of `System.Threading.Thread` constructor.
- *background*  (`bool`):
    If `true` (default), sets `System.Threading.Thread.IsBackground` = `true`. The process ends when the main thread and all foreground threads end; background threads then are terminated.
- *sta*  (`bool`):
    If `true` (default), sets `System.Threading.ApartmentState.STA`.
- *init*  (`Action`):
    Called in the new thread before *threadProc*. This function (`run.thread`) waits until it returns.

##### Returns

`SafeWaitHandle`

Thread handle. Don't forget to dispose.

##### Exceptions

- `OutOfMemoryException`