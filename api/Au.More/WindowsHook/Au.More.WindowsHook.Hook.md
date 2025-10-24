# Method `Au.More.WindowsHook.Hook`

Sets the hook.

```
public void Hook(int threadId = 0)
```

##### Parameters

- *threadId*  (`int`):
    If the hook type is a thread hook - thread id, or 0 for current thread. Else not used and must be 0.

##### Exceptions

- `Au.Types.AuException`:
    Failed.
- `InvalidOperationException`:
    The hook is already set.
- `ArgumentException`:
    *threadId* not 0 and the hook type is not a thread hook.

#### Remarks

Usually don't need to call this function, because the `WindowsHook` static methods that return a new `WindowsHook` object by default call it.