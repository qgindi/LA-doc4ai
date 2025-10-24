# Struct `Au.More.RegisteredHotkey`

Registers a hotkey using API `RegisterHotKey`. Unregisters when disposing.

```
public struct RegisteredHotkey : IDisposable
```

##### Remarks

Can be used as a lightweight alternative to hotkey triggers.

The variable must be disposed, either explicitly (call `Au.More.RegisteredHotkey.Dispose` or `Au.More.RegisteredHotkey.Unregister`) or with `using`.

##### Examples

```
using System.Windows;
using System.Windows.Interop;

new DialogClass().ShowDialog();

class DialogClass : Window {
	RegisteredHotkey _hk1, _hk2;
	
	public DialogClass() {
		Title = "Hotkeys";
		var b = new wpfBuilder(this).WinSize(250);
		b.R.AddOkCancel();
		b.End();
	}

	protected override void OnSourceInitialized(EventArgs e) {
		base.OnSourceInitialized(e);
		var hs = PresentationSource.FromVisual(this) as HwndSource;
		hs.AddHook(_WndProc);
		bool r1 = _hk1.Register(1, "Ctrl+Alt+F10", this);
		bool r2 = _hk2.Register(2, (KMod.Ctrl | KMod.Shift, KKey.D), this); //Ctrl+Shift+D
		print.it(r1, r2);
	}

	protected override void OnClosed(EventArgs e) {
		base.OnClosed(e);
		_hk1.Unregister();
		_hk2.Unregister();
	}

	IntPtr _WndProc(IntPtr hwnd, int msg, IntPtr wParam, IntPtr lParam, ref bool handled) {
		if (msg == RegisteredHotkey.WM_HOTKEY) print.it(wParam);

		return default;
	}
}
```

### Fields

`WM_HOTKEY`

### Methods

`Dispose`, `Register`, `Unregister`

### See Also

`Au.keys.waitForHotkey`