# Method `Au.wnd.ShowL`

Shows (if hidden) or hides this window.

```
public bool ShowL(bool show)
```

##### Parameters

- *show*  (`bool`)

##### Returns

`bool`

Returns `false` if failed. Supports `Au.lastError`.

#### Remarks

Does not activate/deactivate/zorder.

There are two similar functions to show/hide a window:

- `Au.wnd.Show` is better to use in automation scripts, with windows of any process/thread. It calls `ShowL`, and throws exception if it fails. Adds a small delay if the window is of another thread.
- `ShowL` is better to use in programming, with windows of current thread. It is more lightweight. Does not throw exceptions. Does not add a delay. But both functions can be used with windows of any thread.