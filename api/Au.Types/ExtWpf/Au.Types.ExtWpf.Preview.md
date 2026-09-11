# Method `Au.Types.ExtWpf.Preview`

Shows the window in [preview mode](🔗).

```csharp
public static void Preview(this Window t)
```

##### Parameters

- *t*  (`Window`)

##### Exceptions

- `InvalidOperationException`:
  Called not in WPF preview mode.

#### Remarks

Changes some window properties (owner window, location, activation, etc), terminates previous preview process, calls `System.Windows.Window.ShowDialog`. If closed, calls `System.Environment.Exit`.

If called not in preview mode, calls `System.Environment.Exit`.