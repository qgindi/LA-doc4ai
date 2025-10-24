# Property `Au.elmFinder.Next`

Gets or sets next finder in path (immediately after this finder).

```
public elmFinder Next { get; set; }
```

##### Exceptions

- `ArgumentException`:
    *flags* contains `UIA` or `ClientArea`.

##### Property Value

`Au.elmFinder`

#### Remarks

The setter creates or modifies a path (a chain of linked finders). Unlike `Au.elmFinder.this[]`, which appends to the last finder in path, this function appends to this finder.