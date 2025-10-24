# Method `Au.Types.ExtXml.Attr`

## Overload 1

Gets XML attribute value. If the attribute does not exist, returns `null`. If the attribute value is empty, returns `""`.

```
public static string Attr(this XElement t, XName name)
```

##### Parameters

- *t*  (`XElement`)
- *name*  (`XName`)

##### Returns

`string`

* * *

## Overload 2

Gets XML attribute value. If the attribute does not exist, returns *defaultValue*. If the attribute value is empty, returns `""`.

```
public static string Attr(this XElement t, XName name, string defaultValue)
```

##### Parameters

- *t*  (`XElement`)
- *name*  (`XName`)
- *defaultValue*  (`string`)

##### Returns

`string`

* * *

## Overload 3

Gets XML attribute value. If the attribute does not exist, sets *value* = `null` and returns `false`.

```
public static bool Attr(this XElement t, out string value, XName name)
```

##### Parameters

- *t*  (`XElement`)
- *value*  (`string`)
- *name*  (`XName`)

##### Returns

`bool`

* * *

## Overload 4

Gets attribute value converted to `int` number. If the attribute does not exist, returns *defaultValue*. If the attribute value is empty or does not begin with a valid number, returns 0.

```
public static int Attr(this XElement t, XName name, int defaultValue)
```

##### Parameters

- *t*  (`XElement`)
- *name*  (`XName`)
- *defaultValue*  (`int`)

##### Returns

`int`

* * *

## Overload 5

Gets attribute value converted to `int` number. If the attribute does not exist, sets *value* = 0 and returns `false`. If the attribute value is empty or does not begin with a valid number, sets *value* = 0 and returns `true`.

```
public static bool Attr(this XElement t, out int value, XName name)
```

##### Parameters

- *t*  (`XElement`)
- *value*  (`int`)
- *name*  (`XName`)

##### Returns

`bool`

* * *

## Overload 6

Gets attribute value converted to `long` number. If the attribute does not exist, sets *value* = 0 and returns `false`. If the attribute value is empty or does not begin with a valid number, sets *value* = 0 and returns `true`.

```
public static bool Attr(this XElement t, out long value, XName name)
```

##### Parameters

- *t*  (`XElement`)
- *value*  (`long`)
- *name*  (`XName`)

##### Returns

`bool`

* * *

## Overload 7

Gets attribute value converted to double number. If the attribute does not exist, sets *value* = 0 and returns `false`. If the attribute value is empty or is not a valid number, sets *value* = 0 and returns `true`.

```
public static bool Attr(this XElement t, out double value, XName name)
```

##### Parameters

- *t*  (`XElement`)
- *value*  (`double`)
- *name*  (`XName`)

##### Returns

`bool`

* * *

## Overload 8

Gets attribute value converted to float number. If the attribute does not exist, sets *value* = 0 and returns `false`. If the attribute value is empty or is not a valid number, sets *value* = 0 and returns `true`.

```
public static bool Attr(this XElement t, out float value, XName name)
```

##### Parameters

- *t*  (`XElement`)
- *value*  (`float`)
- *name*  (`XName`)

##### Returns

`bool`

* * *

## Overload 9

Gets attribute value as enum type `T`. If the attribute does not exist, sets *value* = `default` and returns `false`. If the attribute value is not a valid enum member name, sets *value* = *default* and returns `true`.

```
public static bool Attr<T>(this XElement t, out T value, XName name) where T : unmanaged, Enum
```

##### Parameters

- *t*  (`XElement`)
- *value*  (`T`)
- *name*  (`XName`)

##### Returns

`bool`

##### Type Parameters

- `T`