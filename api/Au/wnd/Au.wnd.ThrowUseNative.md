# Method `Au.wnd.ThrowUseNative`

## Overload 1

Throws `Au.Types.AuWndException` that uses the last Windows API error (code and message). Also the message depends on whether the window handle is 0/invalid.

```
public void ThrowUseNative()
```

##### Exceptions

- `Au.Types.AuWndException`

* * *

## Overload 2

Throws `Au.Types.AuWndException` that uses the specified Windows API error code and its message. Also the message depends on whether the window handle is 0/invalid.

```
public void ThrowUseNative(int errorCode)
```

##### Parameters

- *errorCode*  (`int`)

##### Exceptions

- `Au.Types.AuWndException`

* * *

## Overload 3

Throws `Au.Types.AuWndException` that uses *mainMessage* and the last Windows API error (code and message). Also the message depends on whether the window handle is 0/invalid.

```
public void ThrowUseNative(string mainMessage)
```

##### Parameters

- *mainMessage*  (`string`)

##### Exceptions

- `Au.Types.AuWndException`

* * *

## Overload 4

Throws `Au.Types.AuWndException` that uses *mainMessage* and the specified Windows API error code. Also the message depends on whether the window handle is 0/invalid.

```
public void ThrowUseNative(int errorCode, string mainMessage)
```

##### Parameters

- *errorCode*  (`int`)
- *mainMessage*  (`string`)

##### Exceptions

- `Au.Types.AuWndException`