# Method `Au.wnd.GetWindowLong`

Calls API `GetWindowLongPtr`.

```
public nint GetWindowLong(int index)
```

##### Parameters

- *index*  (`int`):
    A constant from `Au.Types.GWL`, or an offset in window memory reserved when registering window class.

##### Returns

`nint`

#### Remarks

Supports `Au.lastError`. In 32-bit process actually calls `GetWindowLong`, because `GetWindowLongPtr` is unavailable.