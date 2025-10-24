# Method `Au.More.Convert2.AesDecryptS`

AES-decrypts data. Calls `Au.More.Convert2.AesDecryptB` and converts the returned `byte[]` to string.

```
public static string AesDecryptS(object data, object key, byte[] IV = null)
```

##### Parameters

- *data*  (`object`):
    Encryped data as `byte[]` or Base64 string.
- *key*  (`object`):
    Encryption key. Can be non-empty string (eg a password) or `byte[]` of length 16 (eg a password hash).
- *IV*  (`byte[]`):
    If used `AesEncryptX` that returns an initialization vector, pass it here.

##### Returns

`string`

##### Exceptions

- `ArgumentException`
- `CryptographicException`