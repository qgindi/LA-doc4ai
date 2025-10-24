# Property `Au.uiimage.MatchIndex`

Gets 0-based index of current matching image instance.

```
public int MatchIndex { get; init; }
```

##### Property Value

`int`

#### Remarks

Can be useful in *also* callback functions. When the *image* argument is a list of images, `MatchIndex` starts from 0 for each list image.