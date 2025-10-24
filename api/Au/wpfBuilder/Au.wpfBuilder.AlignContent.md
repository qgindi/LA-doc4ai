# Method `Au.wpfBuilder.AlignContent`

## Overload 1

Sets content alignment of the last added element.

```
public wpfBuilder AlignContent(HorizontalAlignment? x = null, VerticalAlignment? y = null)
```

##### Parameters

- *x*  (`HorizontalAlignment?`):
    Horizontal alignment.
- *y*  (`VerticalAlignment?`):
    Vertical alignment.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:
    The last added element is not `System.Windows.Controls.Control`.

* * *

## Overload 2

Sets content alignment of the last added element.

```
public wpfBuilder AlignContent(string x = null, string y = null)
```

##### Parameters

- *x*  (`string`):
    Horizontal alignment. String like with `Au.wpfBuilder.Align`.
- *y*  (`string`):
    Vertical alignment.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:
    The last added element is not `System.Windows.Controls.Control`.
- `ArgumentException`:
    Invalid alignment string.