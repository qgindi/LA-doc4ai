# Method `Au.More.StringUtil.StringToIntArray`

Creates `int[]` from string containing space-separated numbers, like `"4 100 -8 0x10"`.

```
public static int[] StringToIntArray(string s)
```

##### Parameters

- *s*  (`string`):
    Decimal or/and hexadecimal numbers separated by single space. If `null` or `""`, returns empty array.

##### Returns

`int[]`

#### Remarks

For vice versa use `string.Join(" ", array)`.