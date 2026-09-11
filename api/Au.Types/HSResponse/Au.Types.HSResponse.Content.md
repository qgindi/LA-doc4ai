# Property `Au.Types.HSResponse.Content`

Raw response content.

```csharp
public byte[] Content { get; set; }
```

##### Property Value

`byte[]`

#### Remarks

The server may send this data compressed (it depends on headers etc).

#### Examples

```csharp
r.Content = text.ToUTF8();
```