# Method `Au.Types.ExtInternet.AddFile`

Adds a file field. Uses `System.Net.Http.MultipartFormDataContent.Add`. Please read remarks about disposing.

```
public static MultipartFormDataContent AddFile(this MultipartFormDataContent t, string name, string file, string contentType = null, string fileName = null)
```

##### Parameters

- *t*  (`MultipartFormDataContent`)
- *name*  (`string`):
    Field name.
- *file*  (`string`):
    File path.
- *contentType*  (`string`):
    `Content-Type` header, for example `"image/png"`.
- *fileName*  (`string`):
    Filename. If `null`, gets from *file*.

##### Returns

`MultipartFormDataContent`

This.

##### Exceptions

- `ArgumentException`:
    See `System.Net.Http.MultipartFormDataContent.Add`.
- `Exception`:
    Exceptions of `Au.filesystem.loadStream`.

#### Remarks

Opens the file and stores the stream in this `System.Net.Http.MultipartFormDataContent` object. Won't auto-close it after uploading. To close files, dispose this `MultipartFormDataContent` object, for example with `using` like in the example. Else the file will remain opened/locked until this process exits or until next garbage collection.

#### Examples

```
using var content = internet.formContent(("name1", "value1"), ("name2", "value2")).AddFile("name3", @"C:\Test\file.png");
string s = internet.http.Post("https://httpbin.org/anything", content).Text();
```