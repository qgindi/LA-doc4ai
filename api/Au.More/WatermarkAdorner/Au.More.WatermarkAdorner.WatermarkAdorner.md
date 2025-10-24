# Constructor of `Au.More.WatermarkAdorner`

Initializes and adds this adorner to the `System.Windows.Documents.AdornerLayer` found by `System.Windows.Documents.AdornerLayer.GetAdornerLayer`.

```
public WatermarkAdorner(Control c, string text)
```

##### Parameters

- *c*  (`Control`):
    The control.
- *text*  (`string`):
    Watermark text.

#### Remarks

In some kinds of windows it may not work unless a parent or ancestor of the control is an `System.Windows.Documents.AdornerDecorator`.