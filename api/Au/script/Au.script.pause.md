# Method `Au.script.pause`

If was pressed the pause key, waits until the user presses it again.

```
public static void pause(string text = null, bool doEvents = false)
```

##### Parameters

- *text*  (`string`):
    Text to display in the "Paused script" UI.
- *doEvents*  (`bool`):
    Process Windows messages and other events while waiting. For example, windows of this thread can respond, and timers of this thread can run.

#### Remarks

The default pause key is `ScrollLock` (`Fn+S`, `Fn+K` or similar). To change, use `Au.script.setup` parameter *pauseKey*. If `script.setup` not called, this function uses `ScrollLock` but does not pause when called the first time.

A script can be paused only if it calls this function. Pausing at a random place would be dangerous and is not supported. Call this function in places where it is safe to pause, and where it makes sense, for example in a loop that preses keys or mouse buttons. To pause/resume, let the user press the pause key.

If the pause key is `CapsLock`, waits if it is toggled, even if was toggled when this script started.

#### Examples

```
script.setup(trayIcon: true, pauseKey: KKey.MediaPlayPause);
using var t = osdText.showTransparentText("         ", -1);
for (int i = 0; i < 1000; i++) {
	script.pause();
	//script.pause("Next: continue the loop.");
	t.Text = i.ToS();
	250.ms();
}
```