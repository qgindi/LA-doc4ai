# Constructor of `Au.keys`

```
public keys(OKey cloneOptions)
```

##### Parameters

- *cloneOptions*  (`Au.Types.OKey`):
    Options to be copied to `Au.keys.Options` of this variable. Usually `opt.key` (current ambient options) or `null` (default options).

#### Examples

```
var k = new keys(null);
k.Options.KeySpeed = 50;
k.AddKeys("Tab // Space").AddRepeat(3).AddText("text").AddKey(KKey.Enter).AddSleep(500);
k.SendNow(); //sends and clears the variable
k.Add("Tab // Space*3", "!text", KKey.Enter, 500); //the same as the above k.AddKeys... line
for(int i = 0; i < 5; i++) k.SendNow(true); //does not clear the variable
```