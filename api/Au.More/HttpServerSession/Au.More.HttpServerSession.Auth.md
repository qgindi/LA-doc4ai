# Method `Au.More.HttpServerSession.Auth`

Performs basic authentication. If fails (either the client did not use basic authentication or *auth* returned `false`), throws exception. The client will receive error 401 (Unauthorized) and can retry.

```
protected void Auth(Func<string, string, bool> auth)
```

##### Parameters

- *auth*  (`Func<string, string, bool>`):
    Callback function. Receives the user name and password. Returns `true` to continue or `false` to fail.

#### Remarks

After successful authentication does not repeat it again when the client sends more messages in this session.

#### Examples

`Au.More.HttpServerSession`