# Send keys, text

Activate a window before sending keys or text to it.

```csharp
var w = wnd.find(1, "*- Notepad++").Activate();
//or: wnd.switchActiveWindow();
```

To send keys, use `Au.keys.send`. To quickly insert code, use snippet `kkKeysSendSnippet`: type `kk` and select from the list. Or click toolbar button **Keys** or **Input recorder**.

```csharp
keys.send("Alt+E P Enter"); //note: the string contains key names, not any text
```

To send text, use prefix `!`. Or `Au.keys.sendt` (snippet `ktKeysSendSnippet`).

```csharp
keys.send("!Text.");
keys.sendt("Text."); //the same
keys.send("^Text."); //send text using keys if possible, eg keys Shift+T for uppercase T
```

Send keys and text.

```csharp
keys.send("Ctrl+A Del", "!Text", "Ctrl+S", "!filename.txt");
```

Change speed and other options. To insert code can be used `speedOptSnippet`.

```csharp
opt.key.KeySpeed = 50;
opt.key.TextSpeed = 20;
opt.key.SleepFinally = 100;
opt.key.TextHow = OKeyText.KeysOrChar;
keys.send("Ctrl+End Enter", "!Looooooooooooooooooooooooooooooooooooooooooooooong text.");
```

Repeat key or character.

```csharp
keys.send("Tab*4"); //Tab 4 times
keys.send("_**20"); //character * 20 times
```

Key down and up.

```csharp
keys.send("Alt*down E P Alt*up");
keys.send("Alt+(E P)"); //the same
```

The best way to send menu access characters:

```csharp
keys.send("Alt+^ep");
```

`Ctrl`+click.

```csharp
Action click = () => mouse.click();
keys.send("Ctrl+", click);
```

Send key raw/fast. [More info](🔗).

```csharp
keys.more.sendKey(KKey.A); //press A
keys.more.sendKey(KKey.Ctrl, true); //Ctrl down
keys.more.sendKey(KKey.Ctrl, false); //Ctrl up
```

Turn off `CapsLock`.

```csharp
if (keys.isCapsLock) keys.more.sendKey(KKey.CapsLock);
```