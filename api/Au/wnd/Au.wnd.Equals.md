# Method `Au.wnd.Equals`

## Overload 1

Returns `true` if `w != null` and `w.Value == this`.

```csharp
public bool Equals(wnd? w)
```

##### Parameters

- *w*  (`Au.wnd?`)

##### Returns

`bool`

* * *

## Overload 2

Returns `true` if *obj* is `Au.wnd` and contains the same window handle.

```csharp
public override bool Equals(object obj)
```

##### Parameters

- *obj*  (`object`)

##### Returns

`bool`

##### Overrides

System.ValueType.Equals(object)

* * *

## Overload 3

Returns `true` if `other == this`.

```csharp
public bool Equals(wnd other)
```

##### Parameters

- *other*  (`Au.wnd`)

##### Returns

`bool`

##### Implements

`IEquatable<T>.Equals(T)`