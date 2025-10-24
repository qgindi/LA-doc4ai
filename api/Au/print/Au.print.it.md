# Method `Au.print.it`

## Overload 1

Writes string to the output.

```
public static void it(string value)
```

##### Parameters

- *value*  (`string`)

#### Remarks

Appends newline (`"\r\n"`), unless text is like `"<>text<nonl>"`.

Can display links, colors, images, etc. More info: [Output tags](../articles/Output%20tags.html).

Where the text goes:

- If redirected, to wherever it is redirected. See `Au.print.writer`.
- Else if using log file (`Au.print.logFile` not `null`), writes to the file.
- Else if using console (`Au.print.isWritingToConsole` returns `true`), writes to console.
- Else if using local `Au.More.PrintServer` (in this process), writes to it.
- Else if exists global `Au.More.PrintServer` (in any process), writes to it.
- Else nowhere.

* * *

## Overload 2

Writes value of any type to the output.

```
public static void it(object value)
```

##### Parameters

- *value*  (`object`):
    Value of any type. If `null`, writes `"null"`.

#### Remarks

If the type is unsigned integer (`uint`, `ulong`, `ushort`, `byte`, `nuint`), writes in hexadecimal format with prefix `"0x"`, unless `Au.print.noHex` `true`.

This overload is used for all types except: strings, arrays, generic collections. They have own overloads; to use this function need to cast to object. For `System.Span<T>` and other ref struct types use `print.it(x.ToString());`.

* * *

## Overload 3

Writes interpolated string to the output.

```
public static void it(print.InterpolatedString value)
```

##### Parameters

- *value*  (`Au.print`.`Au.print.InterpolatedString`):
    Interpolated string. Can contain `:print` format like in the example, to display the value like `Au.print.it(object)`.

#### Examples

```
int[] a = { 1, 2, 3 };
print.it($"a: {a}"); //a: System.Int32[]
print.it($"a: {a:print}"); //a: { 1, 2, 3 }
```

* * *

## Overload 4

Writes an array or generic collection to the output.

```
public static void it<T>(IEnumerable<T> value)
```

##### Parameters

- *value*  (`IEnumerable<T>`):

    Array or generic collection of any type. If `null`, writes `"null"`. The format depends on type:

    - `char[]` - like string.
    - `byte[]` - like `xx-xx-xx`; in hexadecimal, unless `Au.print.noHex` `true`.
    - Other - multiple lines.

##### Type Parameters

- `T`

* * *

## Overload 5

Writes multiple arguments of any type to the output, using separator `", "`.

```
public static void it(object value1, object value2, params object[] more)
```

##### Parameters

- *value1*  (`object`)
- *value2*  (`object`)
- *more*  (`object[]`)

#### Remarks

If a value is `null`, writes `"null"`. If a value is unsigned integer (`uint`, `ulong`, `ushort`, `byte`, `nuint`), writes in hexadecimal format with prefix `"0x"`.

* * *

## Overload 6

Writes binary data to the output, formatted like in a hex editor.

```
public static void it(ReadOnlySpan<byte> value, int columns)
```

##### Parameters

- *value*  (`ReadOnlySpan<byte>`)
- *columns*  (`int`):
    The number of bytes in a row.