# Method `Au.wpfBuilder.Validation`

## Overload 1

Sets a validation callback function for the last added element.

```
public wpfBuilder Validation(Func<FrameworkElement, string> func, Action<FrameworkElement> linkClick = null)
```

##### Parameters

- *func*  (`Func<FrameworkElement, string>`):
    Function that returns an error string if element's value is invalid, else returns `null`.
- *linkClick*  (`Action<FrameworkElement>`):
    If not null, called on error link click. For example can be used to make the element visible.

##### Returns

`Au.wpfBuilder`

#### Remarks

The callback function will be called when clicked button **OK** or **Apply** or a button added with flag `Au.Types.WBBFlags.Validate`. If it returns a non-`null` string, the window stays open and button's *click* callback not called. The string is displayed in a tooltip.

#### Examples

```
var b = new wpfBuilder("Window").WinSize(300);
b.R.Add("Name", out TextBox tName)
	.Validation(o => string.IsNullOrWhiteSpace(tName.Text) ? "Name cannot be empty" : null);
b.R.Add("Count", out TextBox tCount)
	.Validation(o => int.TryParse(tCount.Text, out int i1) && i1 >= 0 && i1 <= 100 ? null : "Count must be 0-100");
b.R.AddOkCancel();
b.End();
if (!b.ShowDialog()) return;
print.it(tName.Text, tCount.Text.ToInt());
```

* * *

## Overload 2

Sets a validation callback function for an element.

```
public wpfBuilder Validation(FrameworkElement e, Func<FrameworkElement, string> func, Action<FrameworkElement> linkClick = null)
```

##### Parameters

- *e*  (`FrameworkElement`)
- *func*  (`Func<FrameworkElement, string>`):
    Function that returns an error string if element's value is invalid, else returns `null`.
- *linkClick*  (`Action<FrameworkElement>`):
    If not null, called on error link click. For example can be used to make the element visible.

##### Returns

`Au.wpfBuilder`

#### Remarks

The callback function will be called when clicked button **OK** or **Apply** or a button added with flag `Au.Types.WBBFlags.Validate`. If it returns a non-`null` string, the window stays open and button's *click* callback not called. The string is displayed in a tooltip.

#### Examples

```
var b = new wpfBuilder("Window").WinSize(300);
b.R.Add("Name", out TextBox tName)
	.Validation(o => string.IsNullOrWhiteSpace(tName.Text) ? "Name cannot be empty" : null);
b.R.Add("Count", out TextBox tCount)
	.Validation(o => int.TryParse(tCount.Text, out int i1) && i1 >= 0 && i1 <= 100 ? null : "Count must be 0-100");
b.R.AddOkCancel();
b.End();
if (!b.ShowDialog()) return;
print.it(tName.Text, tCount.Text.ToInt());
```