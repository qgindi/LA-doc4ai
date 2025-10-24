# Constructor of `Au.More.GdiTextRenderer`

## Overload 1

Object created with this ctor can draw and measure.

```
public GdiTextRenderer(nint hdc, int dpi)
```

##### Parameters

- *hdc*  (`nint`):
    Device context handle. `Dispose` will not release it.
- *dpi*  (`int`)

* * *

## Overload 2

Object created with this ctor can measure only. Uses screen DC.

```
public GdiTextRenderer(int dpi)
```

##### Parameters

- *dpi*  (`int`)