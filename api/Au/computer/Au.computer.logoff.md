# Method `Au.computer.logoff`

Initiates computer logoff (sign out) operation.

```
public static bool logoff(bool force = false)
```

##### Parameters

- *force*  (`bool`):
    Don't allow to cancel. Applications with unsaved changes will be forcibly closed.

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.