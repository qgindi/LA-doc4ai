# Method `Au.Types.JSettings.Reload`

Reloads settings from the file.

```
public bool Reload<T>(out T newSettings) where T : JSettings
```

##### Parameters

- *newSettings*  (`T`):
    Receives a new settings object that inherits the behavior of this object but contains updated values of fields defined in the derived class. If the file does not exist, the fields have default values. If failed, receives this object (unchanged).

##### Returns

`bool`

`false` if failed.

##### Type Parameters

- `T`

#### Remarks

Disposes this object. Does not change field values in it. It will no longer be tracked (e.g., for auto-save); tracking continues with the new object.

#### Examples

Run this 2 times to test how a process of your app auto-reloads settings changed by another process of your app.

```
/*/ ifRunning run; /*/

var sett = Settings.Load();
sett.ModifiedExternally += () => {
	if (!sett.Reload(out sett)) return;
	print.it($"ModifiedExternally. This process: {process.thisProcessId}. {sett}");
};

var b = new wpfBuilder("JSettings example").WinSize(300).Columns(-1, -1, -1);
b.R.AddButton("Print", _ => { print.it(sett); });
b.AddButton("one++", _ => { sett.one++; sett.SaveIfNeed(); });
b.AddButton("two++", _ => { sett.two++; sett.SaveIfNeed(); });
b.Window.Topmost = true;
b.ShowDialog();

record Settings : JSettings {
	public static Settings Load() => Load<Settings>(@"C:\Test\JSettings.json");
	
#pragma warning disable CS0649
	public int one;
	public int two = 100;
}
```