# Property `Au.toolbar.Size`

Toolbar width and height without non-client area when `Au.toolbar.AutoSize` `false`.

```csharp
public Size Size { get; set; }
```

##### Property Value

`Size`

#### Remarks

Non-client area is border and title bar when `Au.toolbar.Border` is `ThreeD`, `Thick`, `Caption` or `CaptionX`.

The unit of measurement depends on `Au.toolbar.DpiScaling`.

This property is updated when resizing the toolbar. It is saved.

#### Examples

```csharp
t.Size = new(300, 40);
```