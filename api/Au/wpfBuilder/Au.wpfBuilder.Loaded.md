# Event `Au.wpfBuilder.Loaded`

When root panel loaded and visible. Once.

```
public event Action Loaded
```

#### **Remarks**

If the panel is in a `System.Windows.Controls.TabControl`, this event is fired when the tab page is selected/loaded first time. When this event is fired, handles of visible `System.Windows.Interop.HwndHost`-based controls are already created.