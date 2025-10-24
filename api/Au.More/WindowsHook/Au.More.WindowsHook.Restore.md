# Method `Au.More.WindowsHook.Restore`

Rehooks this low-level keyboard or mouse hook.

```
public void Restore()
```

##### Exceptions

- `InvalidOperationException`:
    The hook type isn't low-level keyboard or mouse.

#### Remarks

Low level hooks may be occasionally disabled by the OS or other hooks. Workaround - call this function eg every 10 s in same thread. For example use `Au.timer`. Don't call too frequently, eg every 1 s. This function unhooks current hook and sets new hook. Ensures that no events are missed or duplicate during it.