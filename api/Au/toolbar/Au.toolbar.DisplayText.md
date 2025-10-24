# Property `Au.toolbar.DisplayText`

Display button text. Default `true`. If `false`, displays text in tooltips, and only displays first 2 characters for buttons without image.

```
public bool DisplayText { get; set; }
```

##### Property Value

`bool`

#### Remarks

A button can override this property:

- To never display text, let its text be empty, like `""` or `"|Tooltip"`.
- To always display text, append `"\a"`, like `"Text\a"` or `"Text\a|Tooltip"`.