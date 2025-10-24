# Method `Au.More.FastBuffer<T>.More`

## Overload 1

Allocates new bigger buffer of specified length. Frees old buffer if need.

```
public void More(int n, bool preserve = false)
```

##### Parameters

- *n*  (`int`):
    Number of elements of type `T`.
- *preserve*  (`bool`):
    Copy previous buffer contents to the new buffer.

##### Exceptions

- `ArgumentException`:
    *n* \<= current buffer length.

* * *

## Overload 2

Allocates new bigger buffer of at least `n*2` length. Frees old buffer if need.

```
public void More(bool preserve = false)
```

##### Parameters

- *preserve*  (`bool`):
    Copy previous buffer contents to the new buffer.