# Method `Au.More.Math2.AlignUp`

## Overload 1

If *value* is divisible by *alignment*, returns *value*. Else returns the nearest bigger number that is divisible by *alignment*.

```
public static int AlignUp(int value, uint alignment)
```

##### Parameters

- *value*  (`int`):
    An integer value.
- *alignment*  (`uint`):
    Alignment. Must be a power of two (2, 4, 8, 16...).

##### Returns

`int`

#### Remarks

For example if *alignment* is 4, returns 4 if *value* is 1-4, returns 8 if *value* is 5-8, returns 12 if *value* is 9-10, and so on.

#### Examples

```
for (int i = 0; i <= 20; i++) print.it(i, Math2.AlignUp(i, 4));
```

* * *

## Overload 2

If *value* is divisible by *alignment*, returns *value*. Else returns the nearest bigger number that is divisible by *alignment*.

```
public static uint AlignUp(uint value, uint alignment)
```

##### Parameters

- *value*  (`uint`):
    An integer value.
- *alignment*  (`uint`):
    Alignment. Must be a power of two (2, 4, 8, 16...).

##### Returns

`uint`

#### Remarks

For example if *alignment* is 4, returns 4 if *value* is 1-4, returns 8 if *value* is 5-8, returns 12 if *value* is 9-10, and so on.

#### Examples

```
for (int i = 0; i <= 20; i++) print.it(i, Math2.AlignUp(i, 4));
```