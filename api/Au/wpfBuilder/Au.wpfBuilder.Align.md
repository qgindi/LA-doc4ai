# Method `Au.wpfBuilder.Align`

## Overload 1

Sets horizontal and/or vertical alignment of the last added element.

```
public wpfBuilder Align(HorizontalAlignment? x = null, VerticalAlignment? y = null)
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
    Current panel is `System.Windows.Controls.Canvas`.

* * *

## Overload 2

Sets horizontal and/or vertical alignment of the last added element.

```
public wpfBuilder Align(string x = null, string y = null)
```

##### Parameters

- *x*  (`string`):
    Horizontal alignment. String that starts with one of these letters, uppercase or lowercase: `L` (left), `R` (right), `C` (center), `S` (stretch).
- *y*  (`string`):
    Vertical alignment. String that starts with one of these letters, uppercase or lowercase: `T` (top), `B` (bottom), `C` (center), `S` (stretch).

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:
    Current panel is `System.Windows.Controls.Canvas`.
- `ArgumentException`:
    Invalid alignment string.