# Property `Au.Types.OKey.Hook`

Callback function that can modify options of "send keys or text" functions depending on active window etc. Default: `null`.

```
public Action<OKeyHookData> Hook { get; set; }
```

##### Property Value

`Action<Au.Types.OKeyHookData>`

#### Remarks

The callback function is called by `Au.keys.send`, `Au.keys.sendt`, `Au.keys.SendNow`, `Au.clipboard.paste` and similar functions. Not called by `Au.clipboard.copy`.

#### Examples

```
opt.key.Hook = k => {
	print.it(k.w);
	var w = k.w.Window; //if k.w is a control, get its top-level window
	var name = w.Name;
	if (name.Like("* Slow App")) {
		k.optk.KeySpeed = 50;
		k.optk.TextSpeed = 50;
	}
};

for (int i = 0; i < 10; i++) {
	1.s();
	keys.send("Home");
}
```

### See Also

`Au.Types.OKeyHookData`