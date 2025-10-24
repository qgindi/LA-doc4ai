# Method `Au.Types.ExtMisc.ToS`

## Overload 1

Converts `double` to `string`. Uses invariant culture, therefore decimal point is always `'.'`, not `','` etc. Calls `double.ToString`.

```
public static string ToS(this double t, string format = null)
```

##### Parameters

- *t*  (`double`)
- *format*  (`string`)

##### Returns

`string`

* * *

## Overload 2

Converts `float` to `string`. Uses invariant culture, therefore decimal point is always `'.'`, not `','` etc. Calls `float.ToString`.

```
public static string ToS(this float t, string format = null)
```

##### Parameters

- *t*  (`float`)
- *format*  (`string`)

##### Returns

`string`

* * *

## Overload 3

Converts `decimal` to `string`. Uses invariant culture, therefore decimal point is always `'.'`, not `','` etc. Calls `decimal.ToString`.

```
public static string ToS(this decimal t, string format = null)
```

##### Parameters

- *t*  (`decimal`)
- *format*  (`string`)

##### Returns

`string`

* * *

## Overload 4

Converts `int` to `string`. Uses invariant culture, therefore minus sign is always ASCII `'-',` not `'−'` etc. Calls `int.ToString`.

```
public static string ToS(this int t, string format = null)
```

##### Parameters

- *t*  (`int`)
- *format*  (`string`)

##### Returns

`string`

* * *

## Overload 5

Converts `long` to `string`. Uses invariant culture, therefore minus sign is always ASCII `'-'`, not `'−'` etc. Calls `double.ToString`.

```
public static string ToS(this long t, string format = null)
```

##### Parameters

- *t*  (`long`)
- *format*  (`string`)

##### Returns

`string`

* * *

## Overload 6

Converts `nint` to `string`. Uses invariant culture, therefore minus sign is always ASCII `'-'`, not `'−'` etc. Calls `nint.ToString`.

```
public static string ToS(this nint t, string format = null)
```

##### Parameters

- *t*  (`nint`)
- *format*  (`string`)

##### Returns

`string`