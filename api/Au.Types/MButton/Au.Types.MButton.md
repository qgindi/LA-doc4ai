# Enum `Au.Types.MButton`

*button* parameter type for `Au.mouse.clickEx` and similar functions.

```
[Flags]
public enum MButton
```

##### Remarks

There are two groups of values:

1. Button (`Left`, `Right`, `Middle`, `X1`, `X2`). Default or 0: `Left`.
2. Action (`Down`, `Up`, `DoubleClick`). Default: click.

Multiple values from the same group cannot be combined. For example `Left|Right` is invalid. Values from different groups can be combined. For example `Right|Down`.

### Fields

| Name | Description |
| --- | --- |
| DoubleClick | (flag) Double-click. |
| Down | (flag) Press and don't release. |
| Left | The left button. |
| Middle | The middle button. |
| Right | The right button. |
| Up | (flag) Don't press, only release. |
| X1 | The 4-th button. |
| X2 | The 5-th button. |