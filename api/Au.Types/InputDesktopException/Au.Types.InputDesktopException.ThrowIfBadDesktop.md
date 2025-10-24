# Method `Au.Types.InputDesktopException.ThrowIfBadDesktop`

Calls `Au.miscInfo.isInputDesktop`. If it returns `false`, throws `Au.Types.InputDesktopException`.

```
public static void ThrowIfBadDesktop(string message = null, bool detectLocked = false)
```

##### Parameters

- *message*  (`string`):
    Message text before the standard message text of this exception.
- *detectLocked*  (`bool`)

##### Exceptions

- `Au.Types.InputDesktopException`