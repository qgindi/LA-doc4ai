# Property `Au.Types.HSResponse.Content`

Raw response content.

```
public byte[] Content { get; set; }
```

##### Property Value

`byte[]`

#### Remarks

The server may send this data compressed (it depends on headers etc).

#### Examples

```
r.Content = text.ToUTF8();
```