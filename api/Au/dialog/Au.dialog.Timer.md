# Event `Au.dialog.Timer`

Every 200 ms.

```csharp
public event Action<DEventArgs> Timer
```

#### **Examples**

```csharp
var d = new dialog("test");
d.Timer += e => { print.it(e.TimerTimeMS); };
d.ShowDialog();
```