# Class `Au.More.PrintServer`

Receives messages sent by `Au.print.it`.

```
public class PrintServer
```

##### Remarks

If server is global, clients can be multiple processes, including this. Else only this process. Works asynchronously, to make writing messages faster. When a client writes a message, the message arrives to the server with some delay and is placed in a queue. You then can get/remove messages from the queue (call `Au.More.PrintServer.GetMessage`) and display them in a window (for example). You can be notified about new messages.

Recommended setup (see example):

1. When your application starts, create a `PrintServer` instance and assign to a static variable. Call `Au.More.PrintServer.Start`.
2. When your application creates its output window, call `Au.More.PrintServer.SetNotifications` to set window/message for notifications.
3. In window procedure, when received the notification message, get/remove/display all new output messages.
4. Call `Au.More.PrintServer.Stop` when closing the window.

##### Examples

Simple program with output window.

```
using System.Windows.Forms;

class OutputFormExample : Form {
	TextBox _tb;

	public OutputFormExample()
	{
		_tb = new TextBox();
		_tb.ReadOnly = true;
		_tb.Multiline = true;
		_tb.ScrollBars = ScrollBars.Both;
		_tb.WordWrap = false;
		_tb.Dock = DockStyle.Fill;
		_tb.TabStop = false;
		this.Controls.Add(_tb);
	}

	protected override void OnHandleCreated(EventArgs e) {
		_os.SetNotifications(this.Hwnd(), WM_APP);
		base.OnHandleCreated(e);
	}

	protected override void WndProc(ref Message m) {
		if(m.Msg == WM_APP) _ProcessMessages();
		base.WndProc(ref m);
	}
	
	internal const int WM_APP = 0x8000;

	void _ProcessMessages()
	{
		while(_os.GetMessage(out var m)) {
			switch(m.Type) {
			case PrintServerMessageType.Clear:
				_tb.Clear();
				break;
			case PrintServerMessageType.Write:
				//_tb.AppendText(m.Text);
				_tb.AppendText($"{DateTime.FromFileTimeUtc(m.TimeUtc).ToLocalTime()}  {m.Caller}  {m.Text}");
				break;
			}
		}
	}

	static PrintServer _os = new(isGlobal: false);

	[STAThread]
	static void Main()
	{
		_os.Start();

		//test Write and Clear, before and after creating window
		print.ignoreConsole = true;
		print.it("test before setting notifications");
		Task.Run(() => { 1.s(); print.it("test after"); 1.s(); print.clear(); 1.s(); print.it("test after Clear"); });

		Application.Run(new OutputFormExample());
		_os.Stop();
	}
}
```

##### Inheritance

`object` → `PrintServer`

### Constructors

`PrintServer(bool)`

### Properties

`MessageCount`, `NoNewline`

### Methods

`GetMessage`, `SetNotifications`, `Start`, `Stop`