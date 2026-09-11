# Event `Au.trayIcon.Message`

When received any message from the tray icon.

```csharp
public event Action<TIEventArgs> Message
```

#### **Remarks**

Receives mouse messages, `NIN_` messages and some other. See `Shell_NotifyIconW`.