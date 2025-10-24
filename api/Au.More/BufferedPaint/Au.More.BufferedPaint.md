# Struct `Au.More.BufferedPaint`

Wraps buffered paint API `BeginBufferedPaint` etc. Must be disposed locally, like in the example.

```
public struct BufferedPaint : IDisposable
```

##### Examples

```
case WM_PAINT:
	using (BufferedPaint bp = new(w, true)) { ... }
	return default;
```

### Constructors

`BufferedPaint(wnd, bool, RECT?)`

### Properties

`DC`, `NonBufferedDC`, `Rect`, `UpdateRect`

### Methods

`Dispose`