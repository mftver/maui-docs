---
layout: post
title: Legend in .NET MAUI Chart control | Syncfusion
description: This section explains about how to enable Legend and its customization in Syncfusion .NET MAUI Chart (SfFunnelChart) control.
platform: maui
control: SfFunnelChart
documentation: ug
---

# Legend in .NET MAUI Funnel Chart

A legend is a graphical representation that explains the meaning of the  data segments in a chart. It typically consists of a key or symbol associated with each data segment and a label that describes what that segment represents. The legend helps users understand the data being presented in the chart by providing a visual reference for the different categories or data points.

{% tabs %}

{% highlight xaml %}

    <chart:SfFunnelChart ItemsSource="{Binding Product}"
                          XBindingPath="Country"
                          YBindingPath="Value">
    <chart:SfFunnelChart.Legend>
        <chart:ChartLegend ></chart:ChartLegend>
    </chart:SfFunnelChart.Legend>
    </chart:SfFunnelChart>
    

{% endhighlight %}

{% highlight c# %}

        SfFunnelChart chart = new SfFunnelChart()
        {
            ItemsSource = this.Product,
            XBindingPath = "Country",
            YBindingPath = "Value",
            
        };

        chart.Series.Add(coffeeSeries);

        ChartLegend legend = new ChartLegend();
        chart.Legend = legend;
        Content = chart;


{% endhighlight %}

{% endtabs %}


![Chart Legend in MAUI Chart](Legend_images/maui_funnelChart_enable_legend.png)


## Legend Visibility

To control the visibility of the legend in a chart control, the [IsVisible]() property can be used. Here's an example of how to define the legend visibility in a chart control:


{% tabs %}

{% highlight xaml %}

    <chart:SfFunnelChart.Legend>
         <chart:ChartLegend IsVisible="True"></chart:ChartLegend>
    </chart:SfFunnelChart.Legend>
   

{% endhighlight %}

{% highlight c# %}
 
    ChartLegend legend = new ChartLegend();
    legend.IsVisible = true;
    chart.Legend = legend;

{% endhighlight %}

{% endtabs %}

## Legend Placement

The Legend were Placed anywhere in the Chart using the [LegendPlacement]() Property.
We can adjust the placement by assigning one of the following values to [legendPlacement]().

* [LegendPlacement.Top]()- Places the legend at the top of the chart.
* [LegendPlacement.Bottom]()- Places the legend at the Bottom of the chart.
* [LegendPlacement.Right]()- Places the legend at the right side of the chart.
* [LegendPlacement.Left]()- Places the legend at the left side of the chart.

N> By default, the [LegendPlacement]() is [LegendPlacement.Top]()

{% tabs %}

{% highlight xaml %}

    <chart:SfFunnelChart.Legend>
        <chart:ChartLegend Placement="Bottom"></chart:ChartLegend>
    </chart:SfFunnelChart.Legend>
   

{% endhighlight %}

{% highlight c# %}
    
    ChartLegend legend = new ChartLegend();
    legend.Placement=LegendPlacement.Bottom;
    chart.Legend = legend;

{% endhighlight %}

{% endtabs %}

![Legend Placement in MAUI Chart](Legend_images/maui_funnelChart_placemant.png)

## Legend Toggle Series Visibility

We can control the visibility of the segments by enabling the [ToggleSeriesVisibility]() property of the ChartLegend. This allows us to toggle the visibility of the segment when the legend items are tapped.

{% tabs %}

{% highlight xaml %}

    <chart:SfFunnelChart.Legend>
        <chart:ChartLegend ToggleSeriesVisibility="True"></chart:ChartLegend>
    </chart:SfFunnelChart.Legend>

{% endhighlight %}

{% highlight c# %}
 
    ChartLegend legend = new ChartLegend();
    legend.ToggleSeriesVisibility = true;
    chart.Legend = legend;

{% endhighlight %}

{% endtabs %}


## Legend Icon Customization

We can able to customize the appearence of the Legend Icon using the [LegendIcon]() in the series.
In [LegendIcon]() property we can use below listed Shapes to Customize the Legend Icon:

| Icon Shapes | Icon Shapes       | Icon Shapes   |
| --------    | --------          | --------      |
| Circle      | Horizontal Line   | Rectangle     |
| Cross       | Inverted Triangle | Triangle      |
| Diamond     | Pentagon          | Vertical Line |
| Hexagon     | Plus              |        |


N> The default value for the LegendIcon in the Series is circular in shape.


{% tabs %}

{% highlight xaml %}

    <chart:SfFunnelChart ItemsSource="{Binding Product}"
                         XBindingPath="Country"
                         YBindingPath="Value"
                         LegendIcon="Triangle">                      
    </chart:SfFunnelChart>

{% endhighlight %}

{% highlight c# %}
 
    SfFunnelChart coffeeSeries = new SfFunnelChart()
    {
      ItemsSource = this.Product,
      XBindingPath = "Country",
      YBindingPath = "Value",
      LegendIcon = ChartLegendIconType.Triangle
    };

    chart.Series.Add(coffeeSeries);

{% endhighlight %}

{% endhighlight %}

{% endtabs %}

![Legend Icon Customization in MAUI Chart](Legend_images/maui_funnelChart_Icon_invertedTriangle.png)

### Series Type Legend Icon

We can Customize the Legend Icon based on the Series type in the Chart.
Each series  has its own legend icon. This can be achieve through the [LegendIcon]() of the series is set to be [SeriesType]().


{% tabs %}

{% highlight xaml %}

    <chart:SfFunnelChart ItemsSource="{Binding Product}"
                         XBindingPath="Country"
                         YBindingPath="Value"
                         LegendIcon="SeriesType">                      
    </chart:SfFunnelChart>

   
{% endhighlight %}

{% highlight c# %}
 
    SfFunnelChart coffeeSeries = new SfFunnelChart()
    {
      ItemsSource = this.Product,
      XBindingPath = "Country",
      YBindingPath = "Value",
      LegendIcon = ChartLegendIconType.SeriesType
    };

    chart.Series.Add(coffeeSeries);

{% endhighlight %}

{% endtabs %}

![Series Type Legend Icon Customization in MAUI Chart](Legend_images/maui_funnelChart_Icon_SeriesType.png)