# Method `Au.keys.SendNow`

Sends keys, text and executes other events added with the `AddX` functions.

```
public void SendNow(bool canSendAgain = false)
```

##### Parameters

- *canSendAgain*  (`bool`):
    Don't clear the internal collection. If `true`, this function then can be called again (eg in loop) to send/execute the same keys etc. If `false` (default), clears the added keys etc; then you can call `AddX` functions and `SendNow` again.

##### Exceptions

- `ArgumentException`:
    *canSendAgain* is `true` and *keys_* end with `+` or `(`.
- `Au.Types.AuException`:
    Failed. For example there is no focused window when sending text.
- `Au.Types.InputDesktopException`