# Method `Au.More.Math2.MulDiv`

Returns `number * multiply / divide`. Multiplies without overflow and rounds up or down to the nearest integer.

```
public static int MulDiv(int number, int multiply, int divide)
```

##### Parameters

- *number*  (`int`)
- *multiply*  (`int`)
- *divide*  (`int`)

##### Returns

`int`

##### Exceptions

- `OverflowException`
- `DivideByZeroException`