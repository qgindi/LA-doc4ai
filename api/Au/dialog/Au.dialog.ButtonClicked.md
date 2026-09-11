# Event `Au.dialog.ButtonClicked`

When the user selects a button.

```csharp
public event Action<DEventArgs> ButtonClicked
```

#### **Examples**

```csharp
var d = new dialog("test", buttons: "1 Can close|2 Can't close");
d.ButtonClicked += e => { print.it(e.Button); e.DontCloseDialog = e.Button == 2; };
d.ShowDialog();
```