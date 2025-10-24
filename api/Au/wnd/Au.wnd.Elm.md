# Property `Au.wnd.Elm`

Gets an `Au.elmFinder` for finding UI elements in this window or control. Example: `var e = w.Elm["ROLE", "Name"].Find();`. Example: `var e = w.Elm["ROLE1", "Name1"]["ROLE2", "Name2"]["ROLE3", "Name3"].Find();`. Example: `print.it(w.Elm.FindAll());`.

```
public elmFinder Elm { get; }
```

##### Property Value

`Au.elmFinder`