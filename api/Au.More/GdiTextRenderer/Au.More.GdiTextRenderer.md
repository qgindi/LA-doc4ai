# Class `Au.More.GdiTextRenderer`

Draws text using fastest GDI API such as `TextOut` and standard UI font. Can easily draw string parts with different colors/styles without measuring. Must be disposed.

```
public class GdiTextRenderer : IDisposable
```

##### Inheritance

`object` → `GdiTextRenderer`

### Constructors

`GdiTextRenderer(int)`, `GdiTextRenderer(nint, int)`

### Methods

`Dispose`, `DrawText`, `DrawText`, `DrawText`, `FontBold`, `FontNormal`, `GetCurrentPosition`, `MeasureText`, `MoveTo`