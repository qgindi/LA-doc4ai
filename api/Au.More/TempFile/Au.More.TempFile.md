# Class `Au.More.TempFile`

Creates unique name for a temporary file and later auto-deletes the file.

```csharp
public sealed class TempFile : IDisposable
```

##### Remarks

Use code like in the example to auto-delete the temporary file if exists. Or call `Au.More.TempFile.Dispose`. Else this class does not delete the file.

##### Examples

```csharp
using (var f = new TempFile()) {
	print.it(f);
	filesystem.saveText(f, "DATA");
	print.it(filesystem.loadText(f));
} //now auto-deletes the file
```

##### Inheritance

`object` → `TempFile`

### Constructors

`TempFile(string, string)`

### Properties

`File`

### Methods

`Dispose`, `ToString`

### Operators

`implicit operator string(TempFile)`