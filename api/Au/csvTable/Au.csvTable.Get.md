# Method `Au.csvTable.Get`

## Overload 1

Gets a field value converted to int. See `Au.Types.ExtString.ToInt`.

```
public bool Get(Index row, int column, out int value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index.
- *column*  (`int`):
    0-based column index.
- *value*  (`int`):
    Receives the result, or 0 if failed.

##### Returns

`bool`

False if failed to convert from string.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.

* * *

## Overload 2

Gets a field value converted to `uint`. See `Au.Types.ExtString.ToInt`.

```
public bool Get(Index row, int column, out uint value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index.
- *column*  (`int`):
    0-based column index.
- *value*  (`uint`):
    Receives the result, or 0 if failed.

##### Returns

`bool`

False if failed to convert from string.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.

* * *

## Overload 3

Gets a field value converted to `long`. See `Au.Types.ExtString.ToInt`.

```
public bool Get(Index row, int column, out long value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index.
- *column*  (`int`):
    0-based column index.
- *value*  (`long`):
    Receives the result, or 0 if failed.

##### Returns

`bool`

False if failed to convert from string.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.

* * *

## Overload 4

Gets a field value converted to `ulong`. See `Au.Types.ExtString.ToInt`.

```
public bool Get(Index row, int column, out ulong value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index.
- *column*  (`int`):
    0-based column index.
- *value*  (`ulong`):
    Receives the result, or 0 if failed.

##### Returns

`bool`

False if failed to convert from string.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.

* * *

## Overload 5

Gets a field value converted to double. See `Au.Types.ExtString.ToNumber`.

```
public bool Get(Index row, int column, out double value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index.
- *column*  (`int`):
    0-based column index.
- *value*  (`double`):
    Receives the result, or 0 if failed.

##### Returns

`bool`

False if failed to convert from string.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.

* * *

## Overload 6

Gets a field value converted to float. See `Au.Types.ExtString.ToNumber`.

```
public bool Get(Index row, int column, out float value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index.
- *column*  (`int`):
    0-based column index.
- *value*  (`float`):
    Receives the result, or 0 if failed.

##### Returns

`bool`

False if failed to convert from string.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.

* * *

## Overload 7

Gets a field value like `"true"` or `"false"` converted to `bool`. Case-insensitive.

```
public bool Get(Index row, int column, out bool value)
```

##### Parameters

- *row*  (`Index`):
    0-based row index.
- *column*  (`int`):
    0-based column index.
- *value*  (`bool`):
    Receives the result, or 0 if failed.

##### Returns

`bool`

False if failed to convert from string.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *row* or *column*.