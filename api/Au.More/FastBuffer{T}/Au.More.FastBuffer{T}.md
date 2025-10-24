# Struct `Au.More.FastBuffer<T>`

Memory buffer on stack with ability to expand and use heap memory. Can be used for calling Windows API or building arrays. Must be used with `[SkipLocalsInit]` attribute; add it to the caller function or class.

```
public ref struct FastBuffer<T> where T : unmanaged
```

##### Type Parameters

| Name | Description |
| --- | --- |
| T |  |

##### Examples

```
print.it(api.GetEnvironmentVariable("temp"));

unsafe class api : NativeApi {
	[DllImport("kernel32.dll", EntryPoint = "GetEnvironmentVariableW", SetLastError = true)]
	static extern int _GetEnvironmentVariable(string lpName, char* lpBuffer, int nSize);

	[SkipLocalsInit]
	internal static string GetEnvironmentVariable(string name) {
		using FastBuffer<char> b = new();
		for (; ; ) if (b.GetString(_GetEnvironmentVariable(name, b.p, b.n), out var s)) return s;
	}
}
```

### Constructors

`FastBuffer()`, `FastBuffer(int)`

### Fields

`StackSize`

### Properties

`this[int]`, `n`, `p`

### Methods

`Dispose`, `FindByteStringLength`, `FindStringLength`, `GetString`, `GetStringFindLength`, `More`, `More`

### Operators

`implicit operator T*(in FastBuffer<T>)`