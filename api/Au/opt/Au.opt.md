# Class `Au.opt`

Ambient options for some functions of this library.

```csharp
public static class opt
```

##### Remarks

Some frequently used functions of this library have some options (settings). For example `Au.keys.send` allows to change speed, text sending method, etc. Passing options as parameters in each call usually isn't what you want to do in automation scripts. Instead use this class. See examples.

To store these options, internally is used `System.Threading.AsyncLocal<T>`. It means that a new task or thread inherits a copy of options of the caller. It can't modify options of the caller or other tasks/threads.

##### Examples

```csharp
opt.key.KeySpeed = 50;
```

Set options for trigger actions.

```csharp
Triggers.Options.BeforeAction = o => { opt.key.KeySpeed = 50; };
```

##### Inheritance

`object` → `opt`

### Properties

`key`, `mouse`, `warnings`