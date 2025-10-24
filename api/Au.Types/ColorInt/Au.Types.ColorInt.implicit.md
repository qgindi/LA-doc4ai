# Operator `Au.Types.ColorInt.implicit operator`

## Overload 1

Converts from an `int` color value in `0xRRGGBB` or `0xAARRGGBB` format. Sets alpha = 0xFF if it is 0 in *color*.

```
public static implicit operator ColorInt(int color)
```

##### Parameters

- *color*  (`int`)

##### Returns

`Au.Types.ColorInt`

* * *

## Overload 2

Converts from an `uint` color value in `0xRRGGBB` or `0xAARRGGBB` format. Sets alpha = 0xFF if it is 0 in *color*.

```
public static implicit operator ColorInt(uint color)
```

##### Parameters

- *color*  (`uint`)

##### Returns

`Au.Types.ColorInt`

* * *

## Overload 3

Converts from `System.Drawing.Color`.

```
public static implicit operator ColorInt(Color color)
```

##### Parameters

- *color*  (`Color`)

##### Returns

`Au.Types.ColorInt`

* * *

## Overload 4

Converts from `System.Windows.Media.Color`.

```
public static implicit operator ColorInt(Color color)
```

##### Parameters

- *color*  (`Color`)

##### Returns

`Au.Types.ColorInt`