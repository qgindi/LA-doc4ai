# Constructor of `Au.Types.RECT`

Sets all fields.

```
[JsonConstructor]
public RECT(int left, int top, int width, int height)
```

##### Parameters

- *left*  (`int`)
- *top*  (`int`)
- *width*  (`int`)
- *height*  (`int`)

#### Remarks

Sets `right = left + width; bottom = top + height;`. To specify right/bottom instead of width/height, use `Au.Types.RECT.FromLTRB` instead.