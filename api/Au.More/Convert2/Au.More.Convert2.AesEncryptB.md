# Method `Au.More.Convert2.AesEncryptB`

## Overload 1

AES-encrypts a `byte[]` or string. Returns `byte[]`.

```
public static byte[] AesEncryptB(object data, object key)
```

##### Parameters

- *data*  (`object`):
    Data to encrypt. Can be `byte[]` or string.
- *key*  (`object`):
    Encryption key. Can be non-empty string (eg a password) or `byte[]` of length 16 (eg a password hash).

##### Returns

`byte[]`

Encrypted data. The first 16 bytes is initialization vector (not secret).

##### Exceptions

- `ArgumentException`
- `CryptographicException`

* * *

## Overload 2

AES-encrypts a `byte[]` or string. Returns `byte[]`.

```
public static byte[] AesEncryptB(object data, object key, out byte[] IV)
```

##### Parameters

- *data*  (`object`):
    Data to encrypt. Can be `byte[]` or string.
- *key*  (`object`):
    Encryption key. Can be non-empty string (eg a password) or `byte[]` of length 16 (eg a password hash).
- *IV*  (`byte[]`):
    Receives an initialization vector. The function generates a random value. Use it with decrypt functions. Don't need to keep it in secret.

##### Returns

`byte[]`

Encrypted data.

##### Exceptions

- `ArgumentException`
- `CryptographicException`