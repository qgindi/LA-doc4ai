# Method `Au.More.Convert2.AesEncryptS`

## Overload 1

AES-encrypts a `byte[]` or string. Calls `Au.More.Convert2.AesEncryptB` and converts the returned `byte[]` to Base64 string.

```
public static string AesEncryptS(object data, object key)
```

##### Parameters

- *data*  (`object`):
    Data to encrypt. Can be `byte[]` or string.
- *key*  (`object`):
    Encryption key. Can be non-empty string (eg a password) or `byte[]` of length 16 (eg a password hash).

##### Returns

`string`

Encrypted data. The first 16 bytes is initialization vector (not secret).

##### Exceptions

- `ArgumentException`
- `CryptographicException`

#### Examples

```
var data = "Encryption example.";
var key = "password";
var enc = Convert2.AesEncryptS(data, key);
print.it(enc);
var dec = Convert2.AesDecryptS(enc, key);
print.it(dec);
```

* * *

## Overload 2

AES-encrypts a `byte[]` or string. Calls `Au.More.Convert2.AesEncryptB` and converts the returned `byte[]` to Base64 string.

```
public static string AesEncryptS(object data, object key, out byte[] IV)
```

##### Parameters

- *data*  (`object`):
    Data to encrypt. Can be `byte[]` or string.
- *key*  (`object`):
    Encryption key. Can be non-empty string (eg a password) or `byte[]` of length 16 (eg a password hash).
- *IV*  (`byte[]`):
    Receives an initialization vector. The function generates a random value. Use it with decrypt functions. Don't need to keep it in secret.

##### Returns

`string`

Encrypted data.

##### Exceptions

- `ArgumentException`
- `CryptographicException`