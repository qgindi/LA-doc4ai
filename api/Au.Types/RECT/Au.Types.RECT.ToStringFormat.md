# Method `Au.Types.RECT.ToStringFormat`

Formats string from `Au.Types.RECT` main fields and properties.

```
public string ToStringFormat(string format)
```

##### Parameters

- *format*  (`string`):
    `System.Text.StringBuilder.AppendFormat` format string. Example: `"({0}, {1}, {4}, {5})"`. This function passes to `AppendFormat` 6 values in this order: `left`, `top`, `right`, `bottom`, `Width`, `Height`.

##### Returns

`string`