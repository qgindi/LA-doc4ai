# Property `Au.opt.key`

Options for keyboard and clipboard functions (classes `Au.keys`, `Au.clipboard` and functions that use them).

```
public static OKey key { get; }
```

##### Property Value

`Au.Types.OKey`

#### Examples

```
opt.key.KeySpeed = 100;
keys.send("Right*10 Ctrl+A");
```

Use a `Au.keys` instance.

```
var k = new keys(opt.key); //create new keys instance and copy options from opt.key to it
k.Options.KeySpeed = 100; //changes option of k but not of opt.key
k.Add("Right*10 Ctrl+A").SendNow(); //uses options of k
```

Set options for trigger actions.

```
Triggers.Options.BeforeAction = o => { opt.key.KeySpeed = 50; };
```