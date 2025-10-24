# Event `Au.More.AppSingleInstance.Notified`

When `Au.More.AppSingleInstance.AlreadyRunning` in new process detected that this process is running. Receives *notifyArgs* passed to it.

```
public static event Action<string[]> Notified
```

#### **Remarks**

To enable this event, call `Au.More.AppSingleInstance.AlreadyRunning` with non-`null` *notifyArgs*. The event handler runs in the same thread. The thread must dispatch Windows messages (for example show a window or dialog, or call `Au.wait.doEvents`).