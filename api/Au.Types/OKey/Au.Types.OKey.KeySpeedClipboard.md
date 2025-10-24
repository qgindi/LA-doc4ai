# Property `Au.Types.OKey.KeySpeedClipboard`

How long to wait (milliseconds) between sending clipboard copy/paste keys. For example, when sending `Ctrl+V`, waits after `Ctrl`-down and after `V`-down. Default: 5.

```
public int KeySpeedClipboard { get; set; }
```

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`int`

Valid values: 0 - 1000 (1 second).

#### Remarks

With most apps these delays are not necessary. But with some apps/controls `Ctrl+V` etc may not work without a delay after `Ctrl`-down or/and after `V`-down.

#### Examples

```
opt.key.KeySpeedClipboard = 50;
```