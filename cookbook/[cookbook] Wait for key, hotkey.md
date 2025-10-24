# Wait for key, hotkey

Wait for key. [More info](/api/Au.keys.waitForKey.html).

```
var key = keys.waitForKey(0, up: false, block: false); //wait for any key
print.it(key);

if (!keys.waitForKey(-5, KKey.Tab, block: true)) return; //wait for <mono>Tab<> and block it. Exit if not pressed in 5 s.
print.it("Tab");
```

Wait for hotkey. [More info](/api/Au.keys.waitForHotkey.html).

```
keys.waitForHotkey(5, "Ctrl+Win+K"); //exception after 5 s
```

Wait until `Ctrl`, `Alt`, `Shift` and `Win` aren't pressed.

```
keys.waitForNoModifierKeys();
```