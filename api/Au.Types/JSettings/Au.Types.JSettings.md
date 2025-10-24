# Class `Au.Types.JSettings`

Base of record classes that contain various settings as public fields or properties. Loads and lazily auto-saves from/to a JSON file.

```
public abstract record JSettings : IDisposable, IEquatable<JSettings>
```

##### Remarks

All functions are thread-safe.

##### Examples

```
MySettings sett = MySettings.Load(); //in a class you would use a static field or property, but this example uses a local variable for simplicity

print.it(sett.i);
sett.i++;

if (dialog.showInput(out string s, "example", editText: sett.s)) {
	sett.s = s;
	
	print.it("old array:", sett.a);
	if ((!sett.a.Contains(s))) sett.a = sett.a.InsertAt(-1, s);
	
	print.it("old dictionary:", sett.d);
	sett.d[s] = DateTime.Now;
}

record class MySettings : JSettings {
	public static readonly string File = folders.ThisAppDocuments + @"MySettings.json";

	public static MySettings Load() => Load<MySettings>(File);
	
	// examples of settings
	public int i;
	public string s = "default";
	public string[] a = [];
	public Dictionary<string, DateTime> d = new();
}
```

##### Inheritance

`object` → `JSettings`

### Properties

`LoadedFile`, `NoAutoSave`, `NoAutoSaveTimer`, `SerializerOptions`

### Methods

`Dispose`, `Dispose`, `Load<T>`, `Reload<T>`, `SaveIfNeed`

### Events

`ModifiedExternally`