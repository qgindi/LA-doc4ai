# Method `Au.Types.ExtString.ToInt`

## Overload 1

Converts part of this string to `int` number and gets the number end index.

```
public static int ToInt(this string t, int startIndex, out int numberEndIndex, STIFlags flags = 0)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *startIndex*  (`int`):
    Offset in this string where to start parsing.
- *numberEndIndex*  (`int`):
    Receives offset in this string where the number part ends. If fails to convert, receives 0.
- *flags*  (`Au.Types.STIFlags`)

##### Returns

`int`

The number, or 0 if failed to convert.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *startIndex* is less than 0 or greater than string length.

#### Remarks

Fails to convert when string is `null`, `""`, does not start with a number or the number is too big.

Unlike `int.Parse` and `System.Convert.ToInt32`:

- The number in string can be followed by more text, like `"123text"`.
- Has *startIndex* parameter that allows to get number from middle, like `"text123text"`.
- Gets the end of the number part.
- No exception when cannot convert.
- The number can be decimal (like `"123"`) or hexadecimal (like `"0x1A"`); don't need separate flags for each style.
- Does not depend on current culture. As minus sign recognizes `'-'` and `'−'`.
- Faster.

The number in string can start with ASCII whitespace (spaces, newlines, etc), like `" 5"`. The number in string can be with `"-"` or `"+"`, like `"-5"`, but not like `"- 5"`. Fails if the number is greater than +- `System.UInt32.MaxValue` (0xffffffff). The return value becomes negative if the number is greater than `System.Int32.MaxValue`, for example `"0xffffffff"` is -1, but it becomes correct if assigned to `uint` (need cast). Does not support non-integer numbers; for example, for `"3.5E4"` returns 3 and sets `numberEndIndex=startIndex+1`.

* * *

## Overload 2

Converts part of this string to `int` number.

```
public static int ToInt(this string t, int startIndex = 0, STIFlags flags = 0)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *startIndex*  (`int`):
    Offset in this string where to start parsing.
- *flags*  (`Au.Types.STIFlags`)

##### Returns

`int`

The number, or 0 if failed to convert.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *startIndex* is less than 0 or greater than string length.

* * *

## Overload 3

Converts part of this string to `int` number and gets the number end index.

```
public static bool ToInt(this string t, out int result, int startIndex, out int numberEndIndex, STIFlags flags = 0)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`int`):
    Receives the result, or 0 if failed.
- *startIndex*  (`int`):
    Offset in this string where to start parsing.
- *numberEndIndex*  (`int`):
    Receives offset in this string where the number part ends. If fails to convert, receives 0.
- *flags*  (`Au.Types.STIFlags`)

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *startIndex* is less than 0 or greater than string length.

* * *

## Overload 4

Converts part of this string to `int` number.

```
public static bool ToInt(this string t, out int result, int startIndex = 0, STIFlags flags = 0)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`int`):
    Receives the result, or 0 if failed.
- *startIndex*  (`int`):
    Offset in this string where to start parsing.
- *flags*  (`Au.Types.STIFlags`)

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *startIndex* is less than 0 or greater than string length.

* * *

## Overload 5

Converts part of this string to `uint` number and gets the number end index.

```
public static bool ToInt(this string t, out uint result, int startIndex, out int numberEndIndex, STIFlags flags = 0)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`uint`):
    Receives the result, or 0 if failed.
- *startIndex*  (`int`):
    Offset in this string where to start parsing.
- *numberEndIndex*  (`int`):
    Receives offset in this string where the number part ends. If fails to convert, receives 0.
- *flags*  (`Au.Types.STIFlags`)

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *startIndex* is less than 0 or greater than string length.

* * *

## Overload 6

Converts part of this string to `uint` number.

```
public static bool ToInt(this string t, out uint result, int startIndex = 0, STIFlags flags = 0)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`uint`):
    Receives the result, or 0 if failed.
- *startIndex*  (`int`):
    Offset in this string where to start parsing.
- *flags*  (`Au.Types.STIFlags`)

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *startIndex* is less than 0 or greater than string length.

* * *

## Overload 7

Converts part of this string to `long` number and gets the number end index.

```
public static bool ToInt(this string t, out long result, int startIndex, out int numberEndIndex, STIFlags flags = 0)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`long`):
    Receives the result, or 0 if failed.
- *startIndex*  (`int`):
    Offset in this string where to start parsing.
- *numberEndIndex*  (`int`):
    Receives offset in this string where the number part ends. If fails to convert, receives 0.
- *flags*  (`Au.Types.STIFlags`)

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *startIndex* is less than 0 or greater than string length.

* * *

## Overload 8

Converts part of this string to `long` number.

```
public static bool ToInt(this string t, out long result, int startIndex = 0, STIFlags flags = 0)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`long`):
    Receives the result, or 0 if failed.
- *startIndex*  (`int`):
    Offset in this string where to start parsing.
- *flags*  (`Au.Types.STIFlags`)

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *startIndex* is less than 0 or greater than string length.

* * *

## Overload 9

Converts part of this string to `ulong` number and gets the number end index.

```
public static bool ToInt(this string t, out ulong result, int startIndex, out int numberEndIndex, STIFlags flags = 0)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`ulong`):
    Receives the result, or 0 if failed.
- *startIndex*  (`int`):
    Offset in this string where to start parsing.
- *numberEndIndex*  (`int`):
    Receives offset in this string where the number part ends. If fails to convert, receives 0.
- *flags*  (`Au.Types.STIFlags`)

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *startIndex* is less than 0 or greater than string length.

* * *

## Overload 10

Converts part of this string to `ulong` number.

```
public static bool ToInt(this string t, out ulong result, int startIndex = 0, STIFlags flags = 0)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`ulong`):
    Receives the result, or 0 if failed.
- *startIndex*  (`int`):
    Offset in this string where to start parsing.
- *flags*  (`Au.Types.STIFlags`)

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *startIndex* is less than 0 or greater than string length.