# Method `Au.wait.s`

## Overload 1

Waits *timeSeconds* seconds. The same as `Au.wait.ms`, but the time is specified in seconds, not milliseconds.

```
public static void s(this int timeSeconds)
```

##### Parameters

- *timeSeconds*  (`int`):
    Time to wait, seconds.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *timeSeconds* is less than 0 or greater than 2147483 (`System.Int32.MaxValue` / 1000, 24.8 days).

#### Remarks

Tip: the script editor replaces code like `100ms` with `100.ms();` when typing.

#### Examples

```
wait.s(5);
5.s(); //the same (s is an extension method)
5000.ms(); //the same
```

* * *

## Overload 2

Waits *timeSeconds* seconds. The same as `Au.wait.ms`, but the time is specified in seconds, not milliseconds.

```
public static void s(this double timeSeconds)
```

##### Parameters

- *timeSeconds*  (`double`):
    Time to wait, seconds. The smallest value is 0.001 (1 ms).

##### Exceptions

- `ArgumentOutOfRangeException`:
    *timeSeconds* is less than 0 or greater than 2147483 (`System.Int32.MaxValue` / 1000, 24.8 days).

#### Examples

```
wait.s(2.5);
2500.ms(); //the same
```