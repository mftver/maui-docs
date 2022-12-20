---
layout: post
title: Trackball in .NET MAUI Chart control | Syncfusion
description: This section explains about how to enable trackball and its customization in Syncfusion .NET MAUI Chart (SfCartesianChart) control.
platform: maui
control: SfCartesianChart
documentation: ug
---

# Trackball in .NET MAUI Chart

Trackball, which allows you to show the tooltip for the nearest data points when you interact with the chart area. On mobile, long press the chart to show the trackball, and drag the chart to change the trackball's location constantly. To display the trackball on the desktop, move the cursor over the chart area.

## Enable Trackball 

To enable the trackball in the chart, create an instance of the [ChartTrackballBehavior]() and set it to the [TrackballBehavior]() property. The following properties are used to show or hide the line and tooltip.

* [ShowMarkers](), of type `bool`, indicates the shows or hides trackball markers. The default value is `True`.
* [ShowLine](), of type `bool`, indicates the shows or hides the trackball line. The default value is `True`.


{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
  ...
   <chart:SfCartesianChart.TrackballBehavior>
      <chart:ChartTrackballBehavior/>
   </chart:SfCartesianChart.TrackballBehavior>
     ...
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

 SfCartesianChart chart = new SfCartesianChart();
 ...
 ChartTrackballBehavior trackball = new ChartTrackballBehavior();
 chart.TrackballBehavior= trackball;

this.Content = chart;

{% endhighlight %}

{% endtabs %}

## Enable Label Display Mode

The [DisplayMode]() property specifies whether a label should be displayed for all data points along the trackball line or only the nearest data point label. The following choices are available for this property.

* `FloatAllPoints` – Displays labels for all the data points along the vertical line.
* `NearestPoint` – Displays label for a single data point nearer to the touch point on the chart area.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
  ...
 <chart:SfCartesianChart.TrackballBehavior>
    <chart:ChartTrackballBehavior ShowLine="True" 
                                  DisplayMode="NearestPoint"/>
 </chart:SfCartesianChart.TrackballBehavior>
     ...
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

 SfCartesianChart chart = new SfCartesianChart();
 ...
 ChartTrackballBehavior trackball = new ChartTrackballBehavior();
 trackball.ShowLine = true;
 trackball.DisplayMode = LabelDisplayMode.NearestPoint;
 . . . 

{% endhighlight %}

{% endtabs %}

## Apperance customization

### Trackball Labels customization

The [LabelStyle]() property provides to customize the trackball labels. These options are:

* `Background`, of type `Brush`, used to change the label background color.
* `Margin`, of type `Thickness`, used to change the margin of the label.
* `TextColor`, of type `Color`, used to change the text color.
* `StrokeWidth`, of type `double`, used to change the stroke thickness of the label.
* `Stroke`, of type `Brush`, used to customize the border of the label.
* `LabelFormat`, of type `string`, used to change the format of the label.
* `FontFamily`, of type `string`, used to change the font family for the trackball label.
* `FontAttributes`, of type `FontAttributes`, used to change the font style for the trackball label.
* `FontSize`, of type `double`, used to change the font size for the trackball label.
* `CornerRadius`, of type `CornerRadius`, used to set the rounded corners for labels.


{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
  ...
   <chart:ChartTrackballBehavior.LabelStyle>
       <chart:ChartLabelStyle Background="LightBlue"   
                              FontSize="15" 
                              CornerRadius="5"
                              StrokeWidth="2" 
                              Stroke="Gray" />
   </chart:ChartTrackballBehavior.LabelStyle>
  ...
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
ChartLabelStyle labelStyle = new ChartLabelStyle();
labelStyle.Background = Colors.LightBlue;
labelStyle.FontSize = 15;
labelStyle.CornerRadius = 5;
labelStyle.StrokeWidth = 2;
labelStyle.Stroke = Colors.Gray;

this.Content = chart;

{% endhighlight %}

{% endtabs %}

### Trackball Line Customization

 The [LineStyle]() property provides to customize the trackball line. These options are:

* `StrokeWidth`, of type `double`, used to change the stroke width of the line.
* `Stroke`, of type `Brush`, used to change the stroke color of the line.
* `StrokeDashArray`, of type `DoubleCollection`, specifies the dashes to be applied on the line.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
   ...
    <chart:ChartTrackballBehavior.LineStyle>
        <chart:ChartLineStyle Stroke="Gray"   
                              StrokeDashArray="4"/>     
    </chart:ChartTrackballBehavior.LineStyle>
...
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
ChartLineStyle lineStyle = new ChartLineStyle();
lineStyle.Stroke = Colors.Gray;
lineStyle.StrokeDashArray = 4;

this.Content = chart;
        
{% endhighlight %}

{% endtabs %}

### Trackball Markers Customization

The [MarkerSettings]() property provides to customize the trackball markers. The trackball marker can be customised using the following properties.

* `Type`, of type `ShapeType`, used to set the marker shape type.
* `Stroke`, of type `Brush`, used to change the marker border color.
* `Fill`, of type `Brush`, used to change the marker background color.
* `StrokeWidth`, of type `double`, used to change the width of the marker border.
* `Width`, of type `double`, used to change the width of the marker.
* `Height`, of type `double`, used to change the height of the marker.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
   ...
    <chart:ChartMarkerSettings Type="InvertedTriangle"  
                               Fill="Brown" 
                               Stroke="Red" 
                               StrokeWidth="1.5"
                               Width="15" 
                               Height="15"/>

...
</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
ChartMarkerSettings markerStyle = new ChartMarkerSettings()
{
   markerStyle.Type = ShapeType.InvertedTriangle,
   markerStyle.Fill = Colors.Brown,
   markerStyle.Stroke = Colors.Red,
   markerStyle.StrokeWidth = 1.5,
   markerStyle.Width = 15,
   markerStyle.Height = 15,
};

this.Content = chart;
        
{% endhighlight %}

{% endtabs %}

## Show or Hide the Series Label

The [CartesianSeries.ShowTrackballLabel]() property is used to show or hide the series trackball label. The default value is `True`.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
   ...
  <chart:LineSeries ShowTrackballLabel="False"
                    ItemsSource="{Binding Data}" 
                    XBindingPath="Name" 
                    YBindingPath="Run"/>  

</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
LineSeries lineSeries = new LineSeries()
{
  ShowTrackballLabel = false,
  XBindingPath = "Name",
  YBindingPath = "Run",
  ItemsSource = new ViewModel().Data

};

this.Content = chart;
        
{% endhighlight %}

{% endtabs %}

## Show or Hide Trackball Label in Axis

When the trackball moves across the axis, this feature highlights the related axis label. The [ChartAxis.ShowTrackballLabel]() property is used to show or hide the axis's trackball label. The [ChartAxis.TrackballLabelStyle]() property is used to customize the appearance of the label. The default value of the [ChartAxis.ShowTrackballLabel]() is `False`.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
   ...
    <chart:CategoryAxis  IsInversed="False" 
                         ShowTrackballLabel="False"/> 

</chart:SfCartesianChart>

{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
. . .
CategoryAxis chartAxis = new CategoryAxis()
{
  chartAxis.IsInversed= false,
  chartAxis.ShowTrackballLabel = false
}

this.Content = chart;
        
{% endhighlight %}

{% endtabs %}

## Methods

* `Show(x, y)` - The [Show]() method is used to activate the trackball at the specified location.
* `Hide()` - The [Hide]() method hides the trackball that is visible in the chart.