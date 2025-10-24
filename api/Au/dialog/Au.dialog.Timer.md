# Event `Au.dialog.Timer`

Every 200 ms.

```
public event Action<DEventArgs> Timer
```

#### **Examples**

```
var d = new dialog("test");
d.Timer += e => { print.it(e.TimerTimeMS); };
d.ShowDialog();
```