# Event `Au.dialog.HyperlinkClicked`

When the user clicks a hyperlink in the dialog text.

```csharp
public event Action<DEventArgs> HyperlinkClicked
```

#### **Examples**

```csharp
var d = new dialog("test", "Text with <a href=\"link data\">links</a>.");
d.HyperlinkClicked += e => { print.it(e.LinkHref); };
d.ShowDialog();
```