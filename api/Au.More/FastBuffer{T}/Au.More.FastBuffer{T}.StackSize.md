# Field `Au.More.FastBuffer<T>.StackSize`

A `Au.More.FastBuffer<T>` variable contains a field of this size. It is a memory buffer on stack. It is a byte count and does not depend on `T`. To get count of `T` elements on stack: `StackSize/sizeof(T)`.

```
public const int StackSize = 2048
```