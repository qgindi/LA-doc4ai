# Method `Au.process.thisThreadHasMessageLoop`

## Overload 1

Returns `true` if this thread has a .NET message loop (winforms or WPF).

```
public static bool thisThreadHasMessageLoop(out bool isWPF)
```

##### Parameters

- *isWPF*  (`bool`):
    Has WPF message loop and no winforms message loop.

##### Returns

`bool`

### See Also

`Au.wnd.getwnd.threadWindows`

* * *

## Overload 2

```
public static bool thisThreadHasMessageLoop()
```

##### Returns

`bool`