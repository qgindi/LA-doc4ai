# Property `Au.trayIcon.Icon`

Gets or sets icon.

```
public icon Icon { get; set; }
```

##### Property Value

`Au.icon`

#### Remarks

To display nice icon at any DPI, the icon should be loaded with `Au.icon.trayIcon` or API `LoadIconMetric`, either from a native resource in your app or from an `.ico` file, which should contain icons of sizes 16, 32 and also recommended 20, 24.