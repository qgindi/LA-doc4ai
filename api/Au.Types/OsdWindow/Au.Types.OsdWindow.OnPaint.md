# Method `Au.Types.OsdWindow.OnPaint`

Called when the OSD window must be drawn or redrawn. Derived classes should override this function and draw anything. Don't need to call `base.OnPaint` of `Au.Types.OsdWindow`, it does nothing.

```
protected virtual void OnPaint(nint dc, Graphics g, RECT r)
```

##### Parameters

- *dc*  (`nint`)
- *g*  (`Graphics`)
- *r*  (`Au.Types.RECT`)

#### Remarks

If `Au.Types.OsdWindow.Opacity` is 0 (default), *g* is filled with `Au.Types.OsdWindow.TransparentColor`. Pixels of this color will be transparent. The base class draws only non-transparent areas.