# Constructor of `Au.More.FastBuffer<T>`

## Overload 1

Allocates first buffer of default size. It is on stack (in this variable), and its length is `StackSize/sizeof(T)` elements of type `T` (2048 bytes or 1024 chars or 512 ints...).

```
public FastBuffer()
```

* * *

## Overload 2

Allocates first buffer of specified size.

```
public FastBuffer(int n)
```

##### Parameters

- *n*  (`int`):
    Buffer length (number of elements of type `T`). If `<= StackSize/sizeof(T)`, the buffer contains` StackSize/sizeof(T)` elements on stack (in this variable); it is 2048 bytes or 1024 chars or 512 ints... Else allocates native memory (much slower).