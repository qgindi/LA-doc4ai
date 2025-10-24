# Enum `Au.Types.TBAnchor`

Used with `Au.toolbar.Anchor`.

```
public enum TBAnchor
```

### Fields

| Name | Description |
| --- | --- |
| All | Anchors are all edges. The toolbar is resized when resizing its owner. |
| BottomLR | Anchors are bottom, left and right edges. The toolbar is resized horizontally when resizing its owner. |
| BottomLeft | Anchors are bottom and left edges. |
| BottomRight | Anchors are bottom and right edges. |
| LeftTB | Anchors are left, top and bottom edges. The toolbar is resized vertically when resizing its owner. |
| OppositeEdgeX | Use owner's opposite left/right edge than specified. In other words, attach toolbar's left edge to owner's right edge or vice versa. This flag is for toolbars that normally are outside of the owner rectangle (at the left or right). This flag cannot be used with `TopLR`, `BottomLR`, `All`. |
| OppositeEdgeY | Use owner's opposite top/bottom edge than specified. In other words, attach toolbar's top edge to owner's bottom edge or vice versa. This flag is for toolbars that normally are outside of the owner rectangle (above or below). This flag cannot be used with `LeftTB`, `RightTB`, `All`. |
| RightTB | Anchors are right, top and bottom edges. The toolbar is resized vertically when resizing its owner. |
| Screen | Anchor is screen, not owner window. Don't move the toolbar together with its owner window. |
| TopLR | Anchors are top, left and right edges. The toolbar is resized horizontally when resizing its owner. |
| TopLeft | Anchors are top and left edges. Default. |
| TopRight | Anchors are top and right edges. |