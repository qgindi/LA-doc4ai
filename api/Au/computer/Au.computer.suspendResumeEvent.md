# Event `Au.computer.suspendResumeEvent`

When the computer is about to enter a suspended state (sleep or hibernate) or has resumed operation after being suspended.

```
public static event Action<PowerModes> suspendResumeEvent
```

#### **Remarks**

Many system events are available in `Microsoft.Win32.SystemEvents` class. For suspend/resume notifications could be used `Microsoft.Win32.SystemEvents.PowerModeChanged`, but it does not work on most computers. Use this event instead.

The event handler is executed in other thread. The parameter can be only `Resume` or `Suspend`. See API `PBT_APMSUSPEND` and `PBT_APMRESUMESUSPEND`.