# Method `Au.wpfBuilder.StartOkCancel`

Adds right-bottom-aligned horizontal stack panel (`Au.wpfBuilder.StartStack`) for adding **OK**, **Cancel** and more buttons. When don't need more buttons, use just `Au.wpfBuilder.AddOkCancel`.

```
public wpfBuilder StartOkCancel()
```

##### Returns

`Au.wpfBuilder`

#### Examples

```
b.StartOkCancel().AddOkCancel().AddButton("Help", _ => {  }).Width(70).End();
```