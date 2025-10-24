# Method `Au.wpfBuilder.Font`

Sets font properties of the last added element and its descendants.

```
public wpfBuilder Font(string name = null, double? size = null, bool? bold = null, bool? italic = null)
```

##### Parameters

- *name*  (`string`):
    If not `null`, sets font name. Can be multiple fonts separated by commas.
- *size*  (`double?`):
    If not `null`, sets font size.
- *bold*  (`bool?`):
    If not `null`, sets font bold or not.
- *italic*  (`bool?`):
    If not `null`, sets font italic or not.

##### Returns

`Au.wpfBuilder`