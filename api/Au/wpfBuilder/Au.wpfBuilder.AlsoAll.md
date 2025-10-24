# Method `Au.wpfBuilder.AlsoAll`

Sets callback function to be called by `AddX` functions for each element added afterwards. Not called by `StartX` functions for panels.

```
public wpfBuilder AlsoAll(Action<wpfBuilder, WBAlsoAllArgs> action)
```

##### Parameters

- *action*  (`Action<Au.wpfBuilder, Au.Types.WBAlsoAllArgs>`):
    Callback function or `null`.

##### Returns

`Au.wpfBuilder`

#### Examples

```
b.AlsoAll((b, e) => {
	if(b.Last is CheckBox c) { c.IsChecked = true; b.Margin("t1 b1"); }
});
```