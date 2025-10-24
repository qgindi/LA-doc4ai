# Method `Au.process.thisProcessExitInvoke`

Calls and removes all `Au.process.thisProcessExit` event handlers.

```
public static void thisProcessExitInvoke()
```

#### Remarks

Call this if `Au.process.thisProcessExit` event handlers don't run because this process is terminated before it. For example when current session is ending (shutdown, restart, logoff); to detect it can be used `Application.SessionEnding`, `Application.OnSessionEnding` or `WM_QUERYENDSESSION`.