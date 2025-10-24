# Constructor of `Au.More.SpeakVoice`

Creates a text-to-speech (speech synthesis) voice instance.

```
public SpeakVoice(string voice = null)
```

##### Parameters

- *voice*  (`string`):
    A voice name from **Control Panel > Speech > Text to speech**. Can be partial, case-insensitive. Example: `"Zira"`. If `null`, uses default voice.