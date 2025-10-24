# Property `Au.Types.OWarnings.Verbose`

If `true`, some library functions may display more warnings and other info.

```
public bool Verbose { get; set; }
```

##### Property Value

`bool`

#### Remarks

If not explicitly set, the default value depends on the build configuration of the main assembly: `true` if Debug, `false` if Release (`optimize true`).

#### Examples

```
opt.warnings.Verbose = false;
```