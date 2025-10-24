# Method `Au.internet.ping`

## Overload 1

Sends an ICMP echo message to the specified website and returns `true` if successful. Can be used to check Internet connectivity.

```
public static bool ping(string hostNameOrAddress = "google.com", int timeout = 5000)
```

##### Parameters

- *hostNameOrAddress*  (`string`):
    Domain name like `"google.com"` or IP like `"123.45.67.89"`.
- *timeout*  (`int`):
    Timeout in milliseconds.

##### Returns

`bool`

#### Remarks

Not all websites support it.

Uses `System.Net.NetworkInformation.Ping`.

* * *

## Overload 2

Sends an ICMP echo message to the specified website and returns `true` if successful. Gets the roundtrip time.

```
public static bool ping(out int roundtripTime, string hostNameOrAddress = "google.com", int timeout = 5000)
```

##### Parameters

- *roundtripTime*  (`int`):
    `System.Net.NetworkInformation.PingReply.RoundtripTime`.
- *hostNameOrAddress*  (`string`):
    Domain name like `"google.com"` or IP like `"123.45.67.89"`.
- *timeout*  (`int`):
    Timeout in milliseconds.

##### Returns

`bool`

#### Remarks

Not all websites support it.

Uses `System.Net.NetworkInformation.Ping`.