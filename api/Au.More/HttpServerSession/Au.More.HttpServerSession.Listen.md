# Method `Au.More.HttpServerSession.Listen`

Simple HTTP 1.1 server.

```
public static void Listen<TSession>(int port = 4455, string ip = null, Action<TcpListener> started = null) where TSession : HttpServerSession, new()
```

##### Parameters

- *port*  (`int`):
    TCP port. Default 4455. If 0, uses the first available port in the dynamic/private ports range (49152-65535); you can use the *started* callback to discover it.
- *ip*  (`string`):
    A local IPv4 or IPv6 address, like `"127.0.0.1"` or `"[::1]"`. If `null` (default), uses `System.Net.IPAddress.IPv6Any` and dual mode (supports IPv6 and IPv4 connections).
- *started*  (`Action<TcpListener>`):
    Called when the server started (after `System.Net.Sockets.TcpListener.Start`).

##### Exceptions

- `Exception`:
    Exceptions of `System.Net.Sockets.TcpListener` functions. Unlikely.

##### Type Parameters

- `TSession`

#### Remarks

Runs all the time and listens for new TCP client connections. For each connected client starts new thread, creates new object of your `Au.More.HttpServerSession`-based type, and calls `Au.More.HttpServerSession.Run`, which calls `Au.More.HttpServerSession.MessageReceived`. Supports keep-alive. Multiple sessions can run simultaneously.

Uses `System.Net.Sockets.TcpListener`, not `System.Net.HttpListener`, therefore don't need administrator privileges, `netsh` and opening ports in firewall. Just the standard firewall dialog first time.

The HTTP server is accessible from local network computers. Usually not accessible from the internet. To make accessible from the internet, you can use ngrok or similar software. This server does not support https (secure connections), but ngrok makes internet connections secure.

The Windows Firewall shows a dialog when the app uses a HTTP server the first time, unless *ip* is `"127.0.0.1"`.

#### Examples

HTTP server.

```
HttpServerSession.Listen<MyHttpSession>();

class MyHttpSession : HttpServerSession {
	//protected override void Run() {
	//	print.it($"Session started. Client IP: {ClientIP}");
	//	base.Run();
	//	print.it("Session ended");
	//}
	
	protected override void MessageReceived(HSMessage m, HSResponse r) {
		//Auth((u, p) => p == "password206474");
		
		print.it(m.Method, m.TargetPath, m.UrlParameters, m.Headers, m.ContentText);
		
		string response = "RESPONSE";
		r.SetContent(response);
		//or
		//r.Content = response.ToUTF8();
		//r.Headers.Add("Content-Type", "text/plain; charset=utf-8");
	}
}
```

HTTP client.

```
var res = internet.http.Get("http://127.0.0.1:4455/file.txt?a=1&b=2"/*, auth: "user:pw"*/).Text(); //from same computer
//var res = internet.http.Get("http://ComputerName:4455/file.txt?a=1&b=2"/*, auth: "user:pw"*/).Text(); //from local network
//var res = internet.http.Get("https://1111-11-111-11-111.ngrok-free.app/file.txt?a=1&b=2"/*, auth: "user:pw"*/).Text(); //from internet through ngrok
print.it(res);
```