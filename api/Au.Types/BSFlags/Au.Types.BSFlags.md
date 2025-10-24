# Enum `Au.Types.BSFlags`

Flags for `Au.More.FastBuffer<T>.GetString`.

```
[Flags]
public enum BSFlags
```

### Fields

| Name | Description |
| --- | --- |
| ReturnsLengthWith0 | The API returns string length including the terminating `'\0'` character. |
| Truncates | If buffer too small, the API gets part of string instead of returning required buffer length. |