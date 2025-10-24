# Select-click menu, control (keyboard shortcuts)

Usually the best way to select/click a menu item is hotkey or `Alt+keys`. It can be recorded with the Input recorder.

```
wnd.find(0, "*- Notepad", "Notepad").Activate();
keys.send("Ctrl+V"); //hotkey
keys.send("Alt+E P"); //Alt+keys
```

Actually with `Alt` should be used characters, not keys, because keys may not work with other keyboard layouts.

```
keys.send("Alt+^ep"); //Alt+characters
```

To select menu items also can be used arrow keys, `Home`, `End`, finally `Enter`. To activate menu bar, use `Alt` or `F10`. To show context menu, use `Apps/Menu` or `Shift+F10`.

Ribbon items (controls) can be selected/clicked in the same way.

Often dialog controls can be selected/clicked in the same way too. Or use `Tab` or `Shift+Tab` to select, `Space` to click, `Alt+Down` to expand combobox, arrows/`Home`/`End` to select list items, `Ctrl+Tab` to select tab pages.

```
wnd.find(1, "* Properties", "#32770").Activate();
keys.send("Alt+^r");
keys.send("Tab*3 Space");
```

When keys can't be used, try UI element functions. See the [UI elements](UI%20elements%20%28find%2C%20click%2C%20check%2C%20focus%2C%20select%2C%20expand%2C%20check%20menu%20item%2C%20wait%20for%20state%2C%20etc%29.html) recipe. Or mouse functions, but scripts with mouse functions may stop working after changing window size, layout or DPI.

See also [keyboard shortcuts and hotkeys in Windows and applications](https://www.google.com/search?q=keyboard+shortcuts+and+hotkeys+in+Windows+and+applications).