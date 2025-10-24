# Class `Au.More.FileWatcher`

Watches a file for external changes. An external change is when another process writes, creates, deletes, moves or renames the file.

```
public sealed class FileWatcher : IDisposable
```

##### Remarks

All functions are thread-safe.

##### Examples

```
/*/ ifRunning run; /*/

var c = new C();
c.Load(@"C:\Test\FileWatcher.xml");
c.ModifyAndSave();
dialog.show("Testing FileWatcher");

class C {
	string _file;
	XElement _x;
	FileWatcher _watcher;
	
	public void Load(string file) {
		_file = file;
		if (filesystem.exists(_file)) {
			_x = XElement.Load(_file);
		} else {
			_x = XElement.Parse("""<a>example</a>""");
		}
		_watcher ??= FileWatcher.Watch(_file, _OnExternalChange);
	}
	
	void _OnExternalChange() {
		_x = XElement.Load(_file);
		print.it("external change", _x);
	}
	
	public void ModifyAndSave() {
		_x.Value = Random.Shared.Next().ToString();
		
		_watcher?.Paused = true;
		try { _x.Save(_file); }
		finally { _watcher?.Paused = false; }
	}
}
```

##### Inheritance

`object` → `FileWatcher`

### Properties

`Paused`

### Methods

`Dispose`, `Watch`