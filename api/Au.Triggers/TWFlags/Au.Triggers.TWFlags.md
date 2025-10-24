# Enum `Au.Triggers.TWFlags`

Flags of window triggers.

```
[Flags]
public enum TWFlags : byte
```

### Fields

| Name | Description |
| --- | --- |
| LaterCallFunc | When using the *later* parameter, call the currently active `Triggers.FuncOf` (see `Au.Triggers.ActionTriggers.FuncOf`) functions on "later" events too. If the function returns `false`, the action will not run. The function runs synchronously in the same thread that called `Au.Triggers.ActionTriggers.Run`. The action runs asynchronously in another thread, which is slower to start. As always, `Triggers.FuncOf` functions must not contain slow code; should take less than 10 ms. |
| RunAtStartup | Run the action when `Au.Triggers.ActionTriggers.Run` called, if the window then is active (for `ActiveOnce` etc triggers) or visible (for `VisibleOnce` etc triggers). |