# Enum `Au.Types.WBBFlags`

Flags for `Au.wpfBuilder.AddButton`.

```
[Flags]
public enum WBBFlags
```

### Fields

| Name | Description |
| --- | --- |
| Apply | It is **Apply** button (size like **OK**/**Cancel**, validates, `Au.wpfBuilder.OkApply` event). |
| Cancel | It is **Cancel** button (`System.Windows.Controls.Button.IsCancel`, closes window). |
| OK | It is **OK** button (`System.Windows.Controls.Button.IsDefault`, closes window, validates, `Au.wpfBuilder.OkApply` event). |
| Validate | Perform validation like **OK** and **Apply** buttons. |