# Method `Au.Types.ExtString.ToNumber`

## Overload 1

Converts this string or its part to double number.

```
public static double ToNumber(this string t, Range? range = null, NumberStyles style = NumberStyles.Float)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *range*  (`Range?`):
    Part of this string or `null` (default).
- *style*  (`NumberStyles`):
    The permitted number format in the string.

##### Returns

`double`

The number, or 0 if failed to convert.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:
    Invalid *style*.

#### Remarks

Calls `double.TryParse` with `System.Globalization.CultureInfo` `InvariantCulture`. Fails if the string is `null` or `""` or isn't a valid floating-point number. Examples of valid numbers: `"12"`, `" -12.3 "`, `".12"`, `"12."`, `"12E3"`, `"12.3e-45"`, `"1,234.5"` (with *style* `NumberStyles.Float | NumberStyles.AllowThousands`). String like `"2text"` is invalid, unless *range* is `0..1`.

* * *

## Overload 2

Converts this string or its part to double number.

```
public static bool ToNumber(this string t, out double result, Range? range = null, NumberStyles style = NumberStyles.Float)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`double`):
    Receives the result, or 0 if failed.
- *range*  (`Range?`):
    Part of this string or `null` (default).
- *style*  (`NumberStyles`):
    The permitted number format in the string.

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:
    Invalid *style*.

#### Remarks

Calls `double.TryParse` with `System.Globalization.CultureInfo` `InvariantCulture`. Fails if the string is `null` or `""` or isn't a valid floating-point number. Examples of valid numbers: `"12"`, `" -12.3 "`, `".12"`, `"12."`, `"12E3"`, `"12.3e-45"`, `"1,234.5"` (with *style* `NumberStyles.Float | NumberStyles.AllowThousands`). String like `"2text"` is invalid, unless *range* is `0..1`.

* * *

## Overload 3

Converts this string or its part to float number.

```
public static bool ToNumber(this string t, out float result, Range? range = null, NumberStyles style = NumberStyles.Float)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`float`):
    Receives the result, or 0 if failed.
- *range*  (`Range?`):
    Part of this string or `null` (default).
- *style*  (`NumberStyles`):
    The permitted number format in the string.

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:
    Invalid *style*.

#### Remarks

Calls `float.TryParse` with `System.Globalization.CultureInfo` `InvariantCulture`.

* * *

## Overload 4

Converts this string or its part to `int` number.

```
public static bool ToNumber(this string t, out int result, Range? range = null, NumberStyles style = NumberStyles.Integer)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`int`):
    Receives the result, or 0 if failed.
- *range*  (`Range?`):
    Part of this string or `null` (default).
- *style*  (`NumberStyles`):
    The permitted number format in the string.

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:
    Invalid *style*.

#### Remarks

Calls `int.TryParse` with `System.Globalization.CultureInfo` `InvariantCulture`.

* * *

## Overload 5

Converts this string or its part to `uint` number.

```
public static bool ToNumber(this string t, out uint result, Range? range = null, NumberStyles style = NumberStyles.Integer)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`uint`):
    Receives the result, or 0 if failed.
- *range*  (`Range?`):
    Part of this string or `null` (default).
- *style*  (`NumberStyles`):
    The permitted number format in the string.

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:
    Invalid *style*.

#### Remarks

Calls `uint.TryParse` with `System.Globalization.CultureInfo` `InvariantCulture`.

* * *

## Overload 6

Converts this string or its part to `long` number.

```
public static bool ToNumber(this string t, out long result, Range? range = null, NumberStyles style = NumberStyles.Integer)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`long`):
    Receives the result, or 0 if failed.
- *range*  (`Range?`):
    Part of this string or `null` (default).
- *style*  (`NumberStyles`):
    The permitted number format in the string.

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:
    Invalid *style*.

#### Remarks

Calls `long.TryParse` with `System.Globalization.CultureInfo` `InvariantCulture`.

* * *

## Overload 7

Converts this string or its part to `ulong` number.

```
public static bool ToNumber(this string t, out ulong result, Range? range = null, NumberStyles style = NumberStyles.Integer)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *result*  (`ulong`):
    Receives the result, or 0 if failed.
- *range*  (`Range?`):
    Part of this string or `null` (default).
- *style*  (`NumberStyles`):
    The permitted number format in the string.

##### Returns

`bool`

`false` if failed.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.
- `ArgumentException`:
    Invalid *style*.

#### Remarks

Calls `ulong.TryParse`. Uses `System.Globalization.CultureInfo.InvariantCulture` if the string range contains only ASCII characters, else uses current culture.