# Keyboard triggers (hotkeys)

To execute some code or run a script, can be used keyboard [triggers](/api/Au.Triggers.ActionTriggers.html) (hotkeys). Examples: `F9`, `Ctrl+K`, `Ctrl+Shift+Alt+H`.

To add a trigger can be used snippet `triggerSnippet` or menu **TT > New trigger**. Add triggers in function `HotkeyTriggers` in file `Hotkey triggers`.

To open a triggers file for editing can be used the **TT** menu.

Click the **Run** button to apply changes after editing.

You'll find hotkey code examples in file `Hotkey triggers`.

Tips:

- To get code for "run script" or "run/open file or URL" you can drag and drop scripts, files and links to the code editor.
- To show hotkey info tools: let the text cursor be in the hotkey string. Then press `Ctrl+Shift+Space`, or invoke the **Keys** window from the **Code** menu or toolbar.
- To quickly insert code `Triggers.Of.Window(...)`, use the quick capturing hotkey (default `Ctrl+Shift+Q`).

See also recipe [Triggers and toolbars](Script%20%27Triggers%20and%20toolbars%27.html).

Also triggers can be used in any script. For example in an `.exe` program that runs without the editor. [Examples](/api/Au.Triggers.ActionTriggers.html).