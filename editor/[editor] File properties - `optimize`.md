# File properties - `optimize`

Whether to make the compiled code as fast as possible.

- `false` (default) - don't optimize. Define preprocessor symbols `DEBUG` and `TRACE` that can be used with `#if`. Aka "Debug configuration".
- `true` (checked) - optimize. Aka "Release configuration".

Default is `false`, because optimization makes difficult to debug. Optimization makes noticeably faster only some types of code, for example processing of large/many arrays. Before deploying class libraries and exe programs you usually compile with `optimize true`.