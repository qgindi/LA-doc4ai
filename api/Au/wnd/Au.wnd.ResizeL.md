# Method `Au.wnd.ResizeL`

Resizes.

```
public bool ResizeL(int width, int height)
```

##### Parameters

- *width*  (`int`)
- *height*  (`int`)

##### Returns

`bool`

#### Remarks

See also `Au.wnd.Resize`. It is better to use in automation scripts, with windows of any process/thread. It throws exceptions, supports optional/reverse/fractional/workarea coordinates, restores if min/max. This function is more lightweight, it just calls API `SetWindowPos` with flags `NOMOVE|NOZORDER|NOOWNERZORDER|NOACTIVATE`. It is better to use in programming, with windows of current thread. Supports `Au.lastError`.

### See Also

`Au.wnd.SetWindowPos`