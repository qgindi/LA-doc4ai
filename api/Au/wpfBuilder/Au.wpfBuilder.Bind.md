# Method `Au.wpfBuilder.Bind`

## Overload 1

Calls `System.Windows.FrameworkElement.SetBinding` of the last added element.

```
public wpfBuilder Bind(DependencyProperty property, string path)
```

##### Parameters

- *property*  (`DependencyProperty`):
    Element's dependency property, for example `TextBox.TextProperty`.
- *path*  (`string`):
    Source property name or path, for example `nameof(MyData.Property)`. Source object should be set with `Au.wpfBuilder.BindingContext`.

##### Returns

`Au.wpfBuilder`

* * *

## Overload 2

Calls `System.Windows.FrameworkElement.SetBinding` of the last added element.

```
public wpfBuilder Bind(DependencyProperty property, BindingBase binding)
```

##### Parameters

- *property*  (`DependencyProperty`):
    Element's dependency property, for example `TextBox.TextProperty`.
- *binding*  (`BindingBase`):
    A binding object, for example `new Binding(nameof(MyData.Property))` or `new Binding(nameof(MyData.Property)) { Source = dataObject }`. In the first case, source object should be set with `Au.wpfBuilder.BindingContext`.

##### Returns

`Au.wpfBuilder`

* * *

## Overload 3

Calls `System.Windows.FrameworkElement.SetBinding` of the last added element and gets its return value.

```
public wpfBuilder Bind(DependencyProperty property, BindingBase binding, out BindingExpressionBase r)
```

##### Parameters

- *property*  (`DependencyProperty`):
    Element's dependency property, for example `TextBox.TextProperty`.
- *binding*  (`BindingBase`):
    A binding object.
- *r*  (`BindingExpressionBase`):
    The return value of `SetBinding`.

##### Returns

`Au.wpfBuilder`

* * *

## Overload 4

Calls `System.Windows.FrameworkElement.SetBinding` of the last added element. Creates `System.Windows.Data.Binding` that uses *source* and *path*.

```
public wpfBuilder Bind(DependencyProperty property, object source, string path)
```

##### Parameters

- *property*  (`DependencyProperty`):
    Element's dependency property, for example `TextBox.TextProperty`.
- *source*  (`object`):
    Data source object.
- *path*  (`string`):
    Source property name or path, for example `nameof(MyData.Property)`.

##### Returns

`Au.wpfBuilder`