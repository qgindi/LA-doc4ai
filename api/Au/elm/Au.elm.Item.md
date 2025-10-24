# Property `Au.elm.Item`

Gets or changes simple element id, also known as child id.

```
public int Item { get; set; }
```

##### Property Value

`int`

#### Remarks

Most UI elements are not simple elements. Then this property is 0. Often (but not always) this property is the 1-based item index in parent. For example `LISTITEM` in `LIST`. The `set` function sometimes can be used as a fast alternative to `Au.elm.Navigate`. It modifies only this variable. It does not check whether the value is valid. Simple elements cannot have child elements.