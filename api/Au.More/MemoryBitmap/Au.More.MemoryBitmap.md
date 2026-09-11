# Class `Au.More.MemoryBitmap`

Creates and manages native bitmap handle and memory DC (GDI device context).
The bitmap is selected in the DC.

```csharp
public class MemoryBitmap : IDisposable
```

##### Inheritance

`object` → `MemoryBitmap`

### Constructors

`MemoryBitmap()`, `MemoryBitmap(int, int)`

### Properties

`Hbitmap`, `Hdc`

### Methods

`Attach`, `Create`, `Delete`, `Detach`, `Dispose`, `Dispose`