# Method `Au.internet.formContent`

Creates an `System.Net.Http.HttpContent` for posting web form fields with functions like `System.Net.Http.HttpClient.PostAsync` and `Au.Types.ExtInternet.Post`.

```
public static MultipartFormDataContent formContent(params (string name, object value)[] fields)
```

##### Parameters

- *fields*  (`(string name, object value)[]`):
    One or more web form field names and values. See example.

##### Returns

`MultipartFormDataContent`

##### Exceptions

- `ArgumentException`:
    An empty name.

#### Examples

```
var content = internet.formContent(("name1", "value1"), ("name2", "value2")).AddFile("name3", @"C:\Test\file.png");
string s = internet.http.Post("https://httpbin.org/anything", content).Text();
```