# Method `Au.Types.WOwner.GetValue`

Gets program name or process id or thread id or owner window. Other variables will be `null`/0.

```
public void GetValue(out wildex program, out int pid, out int tid, out wnd owner)
```

##### Parameters

- *program*  (`Au.wildex`)
- *pid*  (`int`)
- *tid*  (`int`)
- *owner*  (`Au.wnd`)

##### Exceptions

- `ArgumentException`:
    The value is `""` or 0 or contains characters `'\\'` or `'/'` or is invalid wildcard expression.