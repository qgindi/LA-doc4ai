# Event `Au.wpfBuilder.OkApply`

When clicked **OK** or **Apply** button.

```
public event Action<WBButtonClickArgs> OkApply
```

#### **Remarks**

`System.Windows.Controls.Button.IsDefault` is `true` if it is **OK** button. The parameter's property **Cancel** can be used to prevent closing the window.