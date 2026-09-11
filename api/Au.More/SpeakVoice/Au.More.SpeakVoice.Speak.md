# Method `Au.More.SpeakVoice.Speak`

## Overload 1

Speaks the specified text.

```csharp
public void Speak(string text, bool async = false)
```

##### Parameters

- *text*  (`string`):
  Text to speak.
- *async*  (`bool`):
  Don't wait. Note: the sound ends when this process exits.

* * *

## Overload 2

Speaks the specified text.

```csharp
public void Speak(string text, SVFlags flags)
```

##### Parameters

- *text*  (`string`):
  Text to speak.
- *flags*  (`Au.Types.SVFlags`):
  Enum: ASYNC, PURGEBEFORESPEAK, IS_FILENAME, IS_XML, IS_NOT_XML, PERSIST_XML, NLP_SPEAK_PUNC, PARSE_SAPI, PARSE_SSML.