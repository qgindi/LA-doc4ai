# Class `Au.wpfBuilder`

With this class you can create windows with controls, for example for data input.

```
public class wpfBuilder
```

##### Remarks

This class uses WPF (Windows Presentation Foundation). Creates window at run time. No designer. No WPF and XAML knowledge required, unless you want something advanced.

To start, use snippet `wpfDialogSnippet` or menu **File > New > Dialogs**. Also look in Cookbook.

Most functions return `this`, to enable method chaining, aka fluent interface, like with `System.Text.StringBuilder`. See example.

A `wpfBuilder` object can be used to create whole window or some window part, for example a tab page.

The size/position unit in WPF is about 1/96 inch, regardless of screen DPI. For example, if DPI is 96 (100%), 1 unit = 1 physical pixel; if 150% - 1.5 pixel; if 200% - 2 pixels. WPF windows are DPI-scaled automatically when need. Your program's manifest should contain `dpiAware=true/PM` and `dpiAwareness=PerMonitorV2`; it is default for scripts/programs created with the script editor of this library.

Note: WPF starts slowly and uses much memory. It is normal if to show the first window in process takes 500-1000 ms and the process uses 30 MB of memory, whereas WinForms takes 250 ms / 10 MB and native takes 50 ms / 2 MB. However WinForms becomes slower than WPF if there are more than 100 controls in window. This library uses WPF because it is the most powerful and works well with high DPI screens.

WPF has many control types, for example `System.Windows.Controls.Button`, `System.Windows.Controls.CheckBox`, `System.Windows.Controls.TextBox`, `System.Windows.Controls.ComboBox`, `System.Windows.Controls.Label`. Most are in namespaces `System.Windows.Controls` and `System.Windows.Controls.Primitives`. Also on the internet you can find many libraries containing WPF controls and themes. For example, search for *github awesome dotnet C#*. Many libraries are open-source, and most can be found in GitHub (source, info and sometimes compiled files). Compiled files usually can be found in https://www.nuget.org/ as packages. Use menu **Tools > NuGet**.

By default don't need XAML. When need, you can load XAML strings and files with `System.Windows.Markup.XamlReader`.

##### Examples

Dialog window with several controls for data input.

```
var b = new wpfBuilder("Example").WinSize(400); //create Window object with Grid control; set window width 400
b.R.Add("Text", out TextBox text1).Focus(); //add label and text box control in first row
b.R.Add("Combo", out ComboBox combo1).Items("One|Two|Three"); //in second row add label and combo box control with items
b.R.Add(out CheckBox c1, "Check"); //in third row add check box control
b.R.AddOkCancel(); //finally add standard OK and Cancel buttons
b.End();
if (!b.ShowDialog()) return; //show the dialog and wait until closed; return if closed not with OK button
print.it(text1.Text, combo1.SelectedIndex, c1.IsChecked == true); //get user input from control variables
```

##### Inheritance

`object` → `wpfBuilder`

### Constructors

`wpfBuilder(string, WBPanelType)`, `wpfBuilder(FrameworkElement, WBPanelType, bool)`

### Properties

`Last`, `Last2`, `Panel`, `R`, `ResultButton`, `Window`, `gridLines`, `winTopmost`, `winWhite`

### Methods

`Add`, `Add`, `AddButton`, `AddButton`, `AddButton`, `AddOkCancel`, `AddOkCancel`, `AddSeparator`, `Add<T>`, `Add<T>`, `Add<T>`, `Align`, `Align`, `AlignContent`, `AlignContent`, `AlsoAll`, `And`, `Bind`, `Bind`, `Bind`, `Bind`, `BindingContext`, `Border`, `Border`, `Brush`, `Brush`, `Checked`, `Checked`, `Child`, `Columns`, `Disabled`, `Dock`, `Editable`, `End`, `Focus`, `Font`, `FormatText`, `Height`, `Hidden`, `Image`, `Image`, `Items`, `Items`, `Items`, `Items`, `LabeledBy`, `LabeledBy`, `LoadFile`, `Margin`, `Margin`, `Margin`, `Multiline`, `Name`, `Options`, `Padding`, `Padding`, `Padding`, `Readonly`, `Row`, `Select`, `Select`, `ShowDialog`, `Size`, `Skip`, `Span`, `SpanRows`, `Splitter`, `StartCanvas`, `StartCanvas<T>`, `StartCanvas<T>`, `StartDock`, `StartDock<T>`, `StartDock<T>`, `StartGrid`, `StartGrid<T>`, `StartGrid<T>`, `StartOkCancel`, `StartPanel`, `StartPanel<TContainer>`, `StartStack`, `StartStack<T>`, `StartStack<T>`, `Tag`, `Tooltip`, `UiaName`, `Validation`, `Validation`, `Watermark`, `Watermark`, `Width`, `WinProperties`, `WinRect`, `WinSaved`, `WinSize`, `WinXY`, `Wrap`, `Wrap`, `XY`, `formatTextOf`, `formattedText`

### Events

`Loaded`, `OkApply`