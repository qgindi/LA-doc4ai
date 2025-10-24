# Method `Au.keys.AddRepeat`

Adds the repeat operator. Then `Au.keys.SendNow` will send the last added key or character *count* times.

```
public keys AddRepeat(int count)
```

##### Parameters

- *count*  (`int`):
    The repeat count.

##### Returns

`Au.keys`

This.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *count* >10000 or \<0.
- `ArgumentException`:
    The last added item is not a key or single character.