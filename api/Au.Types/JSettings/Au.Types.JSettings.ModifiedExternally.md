# Event `Au.Types.JSettings.ModifiedExternally`

When detected that the settings file was externally modified or deleted (for example by another process of your program).

```
public event Action ModifiedExternally
```

#### **Remarks**

Your event handler can call `Au.Types.JSettings.Reload<T>`.

Runs in a thread pool thread.