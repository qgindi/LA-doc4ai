# Property `Au.elmFinder.ResultGetProperty`

Set this when you need only some property of the UI element (name, etc) and not the UI element itself. The value is a character like with `Au.elm.GetProperties`, for example `'n'` for `Name`. Use `'-'` if you don't need any property.

```
public char ResultGetProperty { set; }
```

##### Exceptions

- `ArgumentException`:
    Used parameter *also*, *navig* or *next*.

##### Property Value

`char`