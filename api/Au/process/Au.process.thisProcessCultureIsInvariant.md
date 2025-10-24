# Property `Au.process.thisProcessCultureIsInvariant`

Gets or sets whether `System.Globalization.CultureInfo.DefaultThreadCurrentCulture` and `System.Globalization.CultureInfo.DefaultThreadCurrentUICulture` are `System.Globalization.CultureInfo.InvariantCulture`.

```
public static bool thisProcessCultureIsInvariant { get; set; }
```

##### Property Value

`bool`

#### Remarks

If your app doesn't want to use current culture (default in .NET apps), it can set these properties = `System.Globalization.CultureInfo.InvariantCulture` or set this property = `true`. It prevents potential bugs when app/script/components don't specify invariant culture in string functions and "number to/from string" functions. Also, there is a bug in "number to/from string" functions in some .NET versions with some cultures: they use wrong minus sign, not ASCII `'-'` which is specified in Control Panel. The default compiler sets this property = `true`; as well as `Au.script.setup`.