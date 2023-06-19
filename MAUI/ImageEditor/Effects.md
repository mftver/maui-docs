---
layout: post
title: Image Effects in .NET MAUI ImageEditor control | Syncfusion
description: Learn here all about Image Effect support in Syncfusion .NET MAUI Image Editor (SfImageEditor) control.
platform: .Net MAUI
control: SfImageEditor
documentation: ug
---

# Image Effect in .NET MAUI Image Editor (SfImageEditor)

Using the image editor control, you can apply various effects such as Brightness, Hue, Saturation, Contrast, Blur, Opacity, and Sharpen to your image. These effects can be applied using the toolbar or by utilizing the `ImageEffect` method. The `ImageEffect` method consists of two arguments: `ImageEffect` and `EffectValue`. The ImageEffect is an enumeration that includes the following effects:

* Brightness
* Blur
* Contrast
* Exposure
* Hue
* Saturation
* Sharpen 
* Opacity
* None

The EffectValue are the corresponding ImageEffect values, which varies for each effect, and they are explained as follows.

N> The Image Effect enum also contains “None” option, which removes all the previously applied effects, which are not saved.
The ImageEffect method only applies the effect to preview image, if you want to save the applied effect you should call SaveEdits method.

## Brightness

Brightness is used to adjust the overall lightness or darkness of the image. The value of the brightness effect ranges from -1 to 1 and the default value is 0.

{% highlight C# %}

public MainPage()
{               
    . . .
    this.imageEditor.ImageEffect(ImageEffect.Brightness, -0.6);
    . . .
}

{% endhighlight %}

## Blur

Blur is used to create a soft and unfocused appearance by reducing the image's sharpness. The value of blur effect ranges from 0 to 1 and the default value is 0.

{% highlight C# %}

public MainPage()
{               
    . . .
    this.imageEditor.ImageEffect(ImageEffect.Blur, 0.5);
    . . .
}

{% endhighlight %}


## Contrast

Contrast is used to increase or decrease the difference between light and dark areas, making the image more visually distinct. The value of contrast effect ranges from -1 to 1 and the default value is 0.

{% highlight C# %}

public MainPage()
{               
    . . .
    this.imageEditor.ImageEffect(ImageEffect. Contrast, -0.8);
    . . .
}

{% endhighlight %}

## Exposure

Exposure is used to alter the overall brightness and darkness levels of the image. The value of the exposure effect ranges from -1 to 1 and the default value is 0.

{% highlight C# %}

public MainPage()
{               
    . . .
    this.imageEditor.ImageEffect(ImageEffect. Exposure, -0.4);
    . . .
}

{% endhighlight %}

## Hue

Hue is used to changes the overall color tone of the image by shifting the color spectrum. The value of hue effect ranges from -1 to 1 and the default value is 0.

{% highlight C# %}

public MainPage()
{               
    . . .
    this.imageEditor.ImageEffect(ImageEffect.Hue, 0.2);
    . . .
}

{% endhighlight %}

## Saturation

Saturation is used to enhance or reduce the intensity and vividness of colors in the image. The value of the saturation effect ranges from -1 to 1 and the default value is 0.

{% highlight C# %}

public MainPage()
{               
    . . .
    this.imageEditor.ImageEffect(ImageEffect. Saturation, -0.8);
    . . .
}

{% endhighlight %}

## Sharpen

Sharpen is used to enhances the clarity and definition of edges and details in the image. The value of sharpen effect ranges from 0 to 6 and the default value is 0.

{% highlight C# %}

public MainPage()
{               
    . . .
    this.imageEditor.ImageEffect(ImageEffect.Sharpen, 0.5);
    . . .
}

{% endhighlight %}

## Opacity

Opacity is used to control the transparency or visibility of the image. The value of the opacity effect ranges from 0 to 1 and the default value is 1.

{% highlight C# %}

public MainPage()
{               
    . . .
    this.imageEditor.ImageEffect(ImageEffect. Opacity, 0.5);
    . . .
}

{% endhighlight %}

## Save or Cancel applied effects

You should call SaveEdits method to save the applied effects in view, otherwise the effects will be reset on next action.

{% highlight C# %}

public MainPage()
{               
    . . .
    this.imageEditor.SaveEdits();
    . . .
}

{% endhighlight %}

The applied effects can be cancelled using CancelEdits method or calling ImageEffect method with ImageEffect.None

{% tabs %}
{% highlight CancelEdits %}

public MainPage()
{               
    . . .
    this.imageEditor.SaveEdits();
    . . .
}

{% endhighlight %}

{% highlight ImageEffect.None %}

public MainPage()
{               
    . . .
    this.imageEditor.ImageEffect(ImageEffect.None, 0);
    . . .
}

{% endhighlight %}
{% endtabs %}