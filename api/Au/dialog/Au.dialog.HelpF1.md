# Event `Au.dialog.HelpF1`

When the user presses `F1`.

```
public event Action<DEventArgs> HelpF1
```

#### **Examples**

```
var d = new dialog("test", "Some info.", footer: "Press F1 for more info.");
d.HelpF1 += e => { run.it("https://www.google.com/search?q=more+info"); };
d.ShowDialog();
```