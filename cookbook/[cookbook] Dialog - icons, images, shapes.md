# Dialog - icons, images, shapes

Some ways of using images in WPF:

- XAML icons from the database. See recipe [button icon, toolbar](Dialog%20-%20button%20icon%2C%20toolbar.html). In the Icons dialog you can find icons and get their name+color.
- `Au.wpfBuilder.Image`. Note: if screen DPI is not 100%, WPF scales non-XAML images and they are a little blurry; there is no easy way to prevent it.

```
using System.Windows;
using System.Windows.Controls;
using System.Windows.Shapes;
using System.Windows.Media;
using System.Windows.Media.Imaging;

var b = new wpfBuilder("Window").WinSize(400);

//XAML icon
b.R.Add(ImageUtil.LoadWpfImageElement("*WeatherIcons.Snow #79AEFF"));

//image file
b.R.Add<Image>().Image(@"C:\Test\screenshot2.png");

//shape
var ellipse = new Ellipse { Stroke = Brushes.BlueViolet, StrokeThickness = 4, Fill = Brushes.LightYellow };
b.R.Add(ellipse).Size(100, 50);

//window icon
b.WinProperties(icon: BitmapFrame.Create(new Uri(@"C:\Test\find.ico")));

if (!b.ShowDialog()) return;
```