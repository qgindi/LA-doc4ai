# Registry

Use class [Registry](https://www.google.com/search?q=C%23+class+Registry). See also [saving variables](Saving%20variables%2C%20settings.html).

Set a string value.

```
Registry.SetValue(@"HKEY_CURRENT_USER\SOFTWARE\Au\Test", "A", "text");
```

Get a string value if exists.

```
if (Registry.GetValue(@"HKEY_CURRENT_USER\SOFTWARE\Au\Test", "A", null) is string s1) {
	print.it(s1);
}
```

Set a `DWORD` value.

```
int i1 = 100;
Registry.SetValue(@"HKEY_CURRENT_USER\SOFTWARE\Au\Test", "B", i1);
```

Get a `DWORD` value if exists.

```
if (Registry.GetValue(@"HKEY_CURRENT_USER\SOFTWARE\Au\Test", "B", null) is int i2) {
	print.it(i2);
}
```

Delete a value if exists.

```
using (var k1 = Registry.CurrentUser.OpenSubKey(@"SOFTWARE\Au\Test", writable: true)) k1.DeleteValue("A", throwOnMissingValue: false);
```

Enumerate subkeys.

```
using (var k1 = Registry.CurrentUser.OpenSubKey(@"SOFTWARE\Microsoft")) {
	foreach (var s2 in k1.GetSubKeyNames()) {
		print.it(s2);
	}
}
```