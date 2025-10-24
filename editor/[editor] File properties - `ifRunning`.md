# File properties - `ifRunning`

When trying to start this script, what to do if it is already running.

- `warn` - print warning and don't run.
- `cancel` - don't run.
- `wait` - run later, when it ends.
- `run` - run simultaneously.
- `restart` - end it and run.
- `end` - end it and don't run.

Suffix `_restart` (`warn_restart`, `cancel_restart`, `wait_restart`, `run_restart`, `end_restart`) changes the behavior: when using the **Run** button/menu to start the script, use `restart`; else use the value as without the suffix.

Default is `warn_restart`.

This property is ignored when the script runs as exe program started not from editor. Then it's an ordinary program (works like with `ifRunning run`). To allow single instance you can use `Au.script.single`, like `script.single("unique string");`.