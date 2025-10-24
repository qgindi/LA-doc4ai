# Method `Au.wnd.getwnd.threadWindows`

Gets top-level windows of a thread.

```
public static wnd[] threadWindows(int threadId, bool onlyVisible = false, bool sortFirstVisible = false)
```

##### Parameters

- *threadId*  (`int`):
    Unmanaged thread id. See `Au.process.thisThreadId`, `Au.wnd.ThreadId`. If 0, throws exception. If other invalid value (ended thread?), returns empty list. Supports `Au.lastError`.
- *onlyVisible*  (`bool`):
    Need only visible windows.
- *sortFirstVisible*  (`bool`):
    Place all array elements of hidden windows at the end of the array, even if the hidden windows are before some visible windows in the Z order.

##### Returns

`Au.wnd[]`

Array containing zero or more `Au.wnd`.

##### Exceptions

- `ArgumentException`:
    *threadId* is 0.

#### Remarks

Calls API `EnumThreadWindows`.

### See Also

`Au.process.thisThreadHasMessageLoop`