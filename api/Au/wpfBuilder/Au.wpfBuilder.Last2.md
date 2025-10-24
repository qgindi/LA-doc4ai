# Property `Au.wpfBuilder.Last2`

Gets the child or descendant element added in current panel before adding `Au.wpfBuilder.Last`. Can be `null`.

```
public FrameworkElement Last2 { get; }
```

##### Property Value

`FrameworkElement`

#### Remarks

For example, after calling an `Add` overload that adds 2 elements (the first is `System.Windows.Controls.Label`), this property returns the `System.Windows.Controls.Label`.