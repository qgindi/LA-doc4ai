# Event `Au.process.thisProcessExit`

Before this process exits, either normally or on unhandled exception.

```
public static event Action<Exception> thisProcessExit
```

#### **Remarks**

The event handler is called on:

- `System.AppDomain.ProcessExit`, with parameter = `null`.
- `System.AppDomain.UnhandledException`, with parameter = the `System.Exception`.