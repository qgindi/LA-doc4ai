# Class `Au.dialog`

Standard dialogs to show information or get user input.

```
public class dialog
```

##### Remarks

You can use static functions like `Au.dialog.show` (less code) or create class instances.

Uses task dialog API `TaskDialogIndirect`.

Cannot be used in services. Instead use `System.Windows.Forms.MessageBox.Show` with option `ServiceNotification` or `DefaultDesktopOnly`, or API `MessageBox` with corresponding flags, or API `WTSSendMessage`.

##### Examples

Simple examples.

```
dialog.show("Example", "Message.);

if(!dialog.showYesNo("Continue?", "More info.")) return;

switch(dialog.show("Save?", "More info.", "1 Save|2 Don't save|0 Cancel")) {
case 1: print.it("save"); break;
case 2: print.it("don't"); break;
default: print.it("cancel"); break;
}

if(!dialog.showInput(out string s, "Example")) return;
print.it(s);
```

This example creates a class instance, sets properties, shows dialog, uses events, uses result.

```
var d = new dialog("Example", "Message.");
d.Buttons("1 OK|2 Cancel|3 Custom|4 Custom2", asCommandLinks: true)
	.Icon(DIcon.Warning)
	.ExpandedText("Expanded info.", true)
	.Checkbox("Check")
	.RadioButtons("1 r1|2 r2")
	.CloseAfter(30, "OK");
d.ButtonClicked += e => { print.it(e.Button); if(e.Button == 4) e.DontCloseDialog = true; };
d.Progress();
d.Timer += e => { e.d.Send.Progress(e.TimerTimeMS / 100); };
var r = d.ShowDialog();
print.it(r, d.Controls.IsChecked, d.Controls.RadioId);
switch(r) { case 1: print.it("OK"); break; case dialog.Timeout: print.it("timeout"); break; }
```

##### Inheritance

`object` → `dialog`

### Constructors

`dialog(string, DText, Strings, DFlags, DIcon, AnyWnd, DText, DText, string, DControls, Coord, Coord, screen, int)`

### Fields

`Timeout`

### Properties

`Controls`, `DialogWindow`, `EditControl`, `IsOpen`, `Result`, `Send`

### Methods

`Buttons`, `ButtonsList`, `Checkbox`, `CloseAfter`, `Default`, `Edit`, `ExpandedText`, `Expander`, `FooterIcon`, `FooterIcon`, `FooterText`, `Icon`, `Icon`, `InScreen`, `OwnerWindow`, `Progress`, `RadioButtons`, `ShowDialog`, `ShowDialogNoWait`, `Text1`, `Text2`, `ThreadWaitForClosed`, `ThreadWaitForOpen`, `Title`, `Wider`, `XY`, `show`, `showError`, `showInfo`, `showInput`, `showInputNumber`, `showList`, `showNoWait`, `showOkCancel`, `showProgress`, `showWarning`, `showYesNo`

### Events

`ButtonClicked`, `Created`, `Destroyed`, `HelpF1`, `HyperlinkClicked`, `OtherEvents`, `Timer`