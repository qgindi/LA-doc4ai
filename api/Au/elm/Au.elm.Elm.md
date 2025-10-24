# Property `Au.elm.Elm`

Gets an `Au.elmFinder` for finding UI elements in this UI element. Example: `var e2 = e1.Elm["ROLE", "Name"].Find();`. Example: `var e2 = e1.Elm["ROLE1", "Name1"]["ROLE2", "Name2"]["ROLE3", "Name3"].Find();`. Example: `print.it(e.Elm.FindAll());`.

```
public elmFinder Elm { get; }
```

##### Property Value

`Au.elmFinder`