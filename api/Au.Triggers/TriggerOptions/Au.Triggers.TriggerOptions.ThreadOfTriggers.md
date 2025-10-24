# Method `Au.Triggers.TriggerOptions.ThreadOfTriggers`

Run trigger actions in the same thread as `Au.Triggers.ActionTriggers.Run`. Dangerous, rarely used.

```
public void ThreadOfTriggers()
```

#### Remarks

This should not be used without a good reason. Trigger actions must be programmed carefully, to not interfere with triggers. They must be as fast as possible, else will block triggers, hooks and user input.

Before v0.16 this was named `Au.Triggers.TriggerOptions.ThreadMain` and used in the `"Triggers and toolbars"` script. Problem: blocks hooks etc when need long time to get file icons. Now the script uses `Au.Triggers.TriggerOptions.ThreadThis` instead, and calls `Triggers.Run` in another thread. Your script possibly still uses the old code. You can replace it with the new version, which can be found in menu **File > New > Default > Triggers and toolbars**.