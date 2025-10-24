# Method `Au.computer.shutdown`

## Overload 1

Initiates computer shutdown or restart operation.

```
public static bool shutdown(bool restart = false, bool force = false, int timeoutS = 0, string message = null, string computer = null)
```

##### Parameters

- *restart*  (`bool`):
    Reboot.
- *force*  (`bool`):
    Don't allow to cancel. Applications with unsaved changes will be forcibly closed.
- *timeoutS*  (`int`):
    The length of time to display the shutdown dialog box, in seconds.
- *message*  (`string`):
    Display this text in the shutdown dialog box and write to the event log.
- *computer*  (`string`):
    The network name of the computer to be shut down. If `null` (default), shuts down this computer. If used, this process must be admin.

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

#### Remarks

Calls API `InitiateSystemShutdown`.

* * *

## Overload 2

Initiates computer shutdown or restart operation.

```
public static bool shutdown(int flags, uint reason = 0)
```

##### Parameters

- *flags*  (`int`):
    `ExitWindowsEx` parameter *uFlags*.
- *reason*  (`uint`):
    `ExitWindowsEx` parameter *dwReason*.

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

#### Remarks

Calls API `ExitWindowsEx`.