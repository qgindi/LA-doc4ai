# Enum `Au.Types.IFAlso`

Used with `Au.uiimage.find` and `Au.uiimage.wait`. Its callback function (parameter *also*) can return one of these values.

```
public enum IFAlso
```

### Fields

| Name | Description |
| --- | --- |
| FindOther | Find more instances of current image. If used list of images, also search for other images. If not found, let the main function return `null` or throw exception or continue waiting; but if a `OkFindX` value used previously, return that result. |
| FindOtherOfList | If used list of images, search for other images. Don't search for more instances of current image. If not found, let the main function return `null` or throw exception or continue waiting; but if a `OkFindX` value used previously, return that result. |
| FindOtherOfThis | Find more instances of current image. When used list of images, don't search for other images. If not found, let the main function return `null` or throw exception or continue waiting; but if a `OkFindX` value used previously, return that result. |
| NotFound | Stop searching. Let the main function return `null` or throw exception or continue waiting. But if a `OkFindX` value used previously, return that result. |
| OkFindMore | Find more instances of current image. If used list of images, also search for other images. Then let the main function return current result. |
| OkFindMoreOfList | If used list of images, search for other images. Don't search for more instances of current image. Then let the main function return current result. |
| OkFindMoreOfThis | Find more instances of current image. When used list of images, don't search for other images. Then let the main function return current result. |
| OkReturn | Stop searching. Let the main function return current result. |