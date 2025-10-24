# Dialog - panels, group box

WPF elements are of 2 main types:

- Controls are visible elements like button, text box and label.
- [Panels](https://www.google.com/search?q=WPF+panels) contain multiple elements (controls, panels) and arrange them in a certain way (table, stack, etc). Panels allow to create UI layouts of any complexity.

Panel types:

- `Au.wpfBuilder.StartGrid` adds a [Grid](https://www.google.com/search?q=WPF+Grid) panel. It's a table with columns and rows. A cell usually contains 1 element, but can contain several or zero. An element can span several cells.
- `Au.wpfBuilder.StartStack` adds a [StackPanel](https://www.google.com/search?q=WPF+StackPanel). It arranges elements in a horizontal or vertical line.
- `Au.wpfBuilder.StartDock` adds a [DockPanel](https://www.google.com/search?q=WPF+DockPanel). It docks elements by its edges specified with `Au.wpfBuilder.Dock`. The last added element fills the remaining space.
- `Au.wpfBuilder.StartCanvas` adds a [Canvas](https://www.google.com/search?q=WPF+Canvas) panel. It does not move/resize elements; for it use `Au.wpfBuilder.XY`.
- `Au.wpfBuilder.StartPanel` adds a panel of another type, for example `WrapPanel`.

The `wpfBuilder` constructor adds the root panel. It's a grid or a panel of specified type. Use the `StartX` functions to add nested panels if need. Call `Au.wpfBuilder.End` to end adding controls to the current panel and return to the parent panel.

The `StartX` functions also can add a container control for the panel, such as `GroupBox` or `Expander`.

```
using System.Windows;
using System.Windows.Controls;
using System.Windows.Media;

var b = new wpfBuilder("Window").WinSize(400);
b.R.Add("Text", out TextBox _).Focus();

//nested stack panel
b.R.StartStack();
	for (int i = 0; i < 5; i++) { b.Add(out CheckBox _, "Check " + i); }
	b.End();

//nested grid panel with a group box
b.R.StartGrid<GroupBox>("Nested grid");
	b.Columns(0, -1, 100);
	b.R.Add("Text 1", out TextBox _).Add(out CheckBox _, "Check");
	b.R.Add("Text 2", out TextBox _).Span(1);

	//nested dock panel inside the grid panel
	b.R.StartDock<GroupBox>("Nested dock panel").Height(80);
		b.Add<Button>("Top").Dock(Dock.Top);
		b.Add<Button>("Left").Dock(Dock.Left);
		b.Add<Button>("Fill");
		b.End(); //end the dock panel

	b.End(); //end the grid panel

b.R.AddOkCancel();

b.End(); //end the root panel. Optional.

if (!b.ShowDialog()) return;
```

In this dialog the root panel is `Canvas`.

```
var bc = new wpfBuilder("Window", WBPanelType.Canvas).WinSize(200, 200);
bc.Add(out TextBox _).XY(10, 10, 70, 30);
bc.Add(out TextBox _).XY(100, 10, 70, 30);
bc.End();
if (!bc.ShowDialog()) return;
```

Add a `WrapPanel`.

```
var bp = new wpfBuilder("Window").WinSize(400, 400);
var wrapPanel = new WrapPanel { ItemWidth = 100 };
bp.StartPanel(wrapPanel);
for (int i = 0; i < 10; i++) { bp.AddButton(i, o => { print.it(o.Button.Content); }); }
bp.End();
if (!bp.ShowDialog()) return;
```