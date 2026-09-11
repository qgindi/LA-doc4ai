# Constructor of `Au.More.EnumUI<T>`

## Overload 1

Adds enum members to a `Au.popupMenu` menu as checkbox-items (if it's a `[Flags]` enum) or radio-items.

```csharp
public EnumUI(popupMenu m, TEnum init = default, (TEnum value, string text)[] items = null, bool sort = false)
```

##### Parameters

- *m*  (`Au.popupMenu`)
- *init*  (`TEnum`):
  Initial value.
- *items*  (`(TEnum value, string text)[]`):
  Enum members and their text/tooltip. Optional. Text can be: `null`, `"text"`, `"text|tooltip"`, `"|tooltip"`.
- *sort*  (`bool`):
  Sort by name.

#### Examples

```csharp
var m = new popupMenu();
var f = new EnumUI<KMod>(m, KMod.Ctrl|KMod.Alt); //a [Flags] enum
m.Separator();
var e = new EnumUI<DayOfWeek>(m, DateTime.Today.DayOfWeek); //a non-[Flags] enum
m.Show();
print.it(f.Result);
print.it(e.Result);
```

### See Also

`popupMenu.AddEnum<TEnum>`

* * *

## Overload 2

Adds members of a `[Flags]` enum as checkboxes to a WPF panel.

```csharp
public EnumUI(Panel container, TEnum init = default, (TEnum value, string text)[] items = null, bool sort = false)
```

##### Parameters

- *container*  (`Panel`):
  `System.Windows.Controls.StackPanel`, `System.Windows.Controls.WrapPanel` or `System.Windows.Controls.Grid`. If `Grid` without columns, adds 2 columns.
- *init*  (`TEnum`):
  Initial value.
- *items*  (`(TEnum value, string text)[]`):
  Enum members and their text/tooltip. Optional. Text can be: `null`, `"text"`, `"text|tooltip"`, `"|tooltip"`.
- *sort*  (`bool`):
  Sort by name.

#### Examples

With `Au.wpfBuilder`.

```csharp
b.R.StartStack(vertical: true);
var e = new EnumUI<KMod>(b.Panel, KMod.Ctrl|KMod.Alt);
b.End();
...
print.it(e.Result);
```

### See Also

[wpfBuilder.AddEnum\[\[lt\]\]TEnum\[\[gt\]\]](🔗)

* * *

## Overload 3

Adds members of a non-`[Flags]` enum to a WPF `System.Windows.Controls.Primitives.Selector` control, for example `System.Windows.Controls.ComboBox`.

```csharp
public EnumUI(Selector container, TEnum init = default, (TEnum value, string text)[] items = null, bool sort = false)
```

##### Parameters

- *container*  (`Selector`)
- *init*  (`TEnum`):
  Initial value.
- *items*  (`(TEnum value, string text)[]`):
  Enum members and their text/tooltip. Optional. Text can be: `null`, `"text"`, `"text|tooltip"`, `"|tooltip"`.
- *sort*  (`bool`):
  Sort by name.

#### Examples

```csharp
b.R.Add("Dock", out ComboBox cb1);
var e = new EnumUI<Dock>(cb1);
...
print.it(e.Result);
```