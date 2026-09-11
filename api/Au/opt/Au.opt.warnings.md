# Property `Au.opt.warnings`

Options for showing run-time warnings and other info that can be useful to find problems in code at run time.

```csharp
public static OWarnings warnings { get; }
```

##### Property Value

`Au.Types.OWarnings`

#### Examples

```csharp
opt.warnings.Verbose = false;
print.warning("Example");
print.warning("Example");
```