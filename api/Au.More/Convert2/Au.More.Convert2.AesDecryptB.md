# Method `Au.More.Convert2.AesDecryptB`

AES-decrypts data. Returns `byte[]`.

```
public static byte[] AesDecryptB(object data, object key, byte[] IV = null)
```

##### Parameters

- *data*  (`object`):
    Encryped data as `byte[]` or Base64 string.
- *key*  (`object`):
    Encryption key. Can be non-empty string (eg a password) or `byte[]` of length 16 (eg a password hash).
- *IV*  (`byte[]`):
    If used `AesEncryptX` that returns an initialization vector, pass it here.

##### Returns

`byte[]`

##### Exceptions

- `ArgumentException`
- `CryptographicException`