---
layout: post
title: Stacked Column Chart in .NET MAUI Chart control | Syncfusion
description: Learn here all about stacked column and bar chart support in Syncfusion .NET MAUI Chart (SfCartesianChart) control.
platform: maui
control: SfCartesianChart
documentation: ug
---

# Stacked Column Chart in .NET MAUI Chart

The stacked column chart represents data values in a stacked format, where the columns are stacked on each other to indicate the cumulative value of the data points.

To render a stacked column chart, create an instance of the [StackedColumnSeries]() and add it to the [Series](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Charts.SfCartesianChart.html#Syncfusion_Maui_Charts_SfCartesianChart_Series) collection property of the [SfCartesianChart](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Charts.SfCartesianChart.html?tabs=tabid-1).

N> The Cartesian chart has [Series](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Charts.SfCartesianChart.html#Syncfusion_Maui_Charts_SfCartesianChart_Series) as its default content.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>

    <chart:SfCartesianChart.XAxes>
    <chart:CategoryAxis />
    </chart:SfCartesianChart.XAxes>

    <chart:SfCartesianChart.YAxes>
        <chart:NumericalAxis />
    </chart:SfCartesianChart.YAxes>

    <chart:StackingColumnSeries ItemsSource="{Binding Data}"
                                XBindingPath="Name"
                                YBindingPath="Value"        
    </chart:StackingColumnSeries>

    <chart:StackingColumnSeries ItemsSource="{Binding Data1}"
                                XBindingPath="Name"
                                YBindingPath="Value"         
    </chart:StackingColumnSeries>

</chart:SfCartesianChart>


{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
CategoryAxis primaryAxis = new CategoryAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

StackingColumnSeries  series = new  StackingColumnSeries()
{
    XBindingPath = "Name",
    YBindingPath = "Value",
    ItemsSource = new ViewModel().Data
};
StackingColumnSeries series1 = new StackingColumnSeries()
{
    XBindingPath = "Name",
    YBindingPath = "Value",
    ItemsSource = new ViewModel().Data1
};

chart.Series.Add(series);
chart.Series.Add(series1);     
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![ Stacked column chart type in MAUI Chart]()

## Grouping Series

Each series in a stacked chart with several series may be difficult to compare. To solve that problem, grouping is used.
The [GroupingLabel]() property used to group the series, which allows users to assign a label to each stacked column series. This label identifies the specific group to which the stacked column series belongs and can be used to group similar series.

N> If the [GroupingLabel]() is not provided, the stacked column will consider all series as a single group.

{% tabs %}

{% highlight xaml %}

<chart:SfCartesianChart>
   
    ....

    <chart:StackingColumnSeries XBindingPath="Name"
                                YBindingPath="Value"
                                ItemsSource="{Binding Data}"
                                GroupingLabel="GroupOne"
    </chart:StackingColumnSeries>

    <chart:StackingColumnSeries XBindingPath="Name"
                                YBindingPath="Value"
                                ItemsSource="{Binding Data1}"
                                GroupingLabel="GroupTwo"
    </chart:StackingColumnSeries>

    <chart:StackingColumnSeries XBindingPath="Name"
                                YBindingPath="Value"
                                ItemsSource="{Binding Data2}"
                                GroupingLabel="GroupOne"
    </chart:StackingColumnSeries>

</chart:SfCartesianChart>


{% endhighlight %}

{% highlight c# %}

SfCartesianChart chart = new SfCartesianChart();
CategoryAxis primaryAxis = new CategoryAxis();
chart.XAxes.Add(primaryAxis);
NumericalAxis secondaryAxis = new NumericalAxis();
chart.YAxes.Add(secondaryAxis);

StackingColumnSeries  series = new  StackingColumnSeries()
{
    XBindingPath = "Name",
    YBindingPath = "Value",
    ItemsSource = new ViewModel().Data,
    GroupingLabel="GroupOne"
};
StackingColumnSeries series1 = new StackingColumnSeries()
{
    XBindingPath = "Name",
    YBindingPath = "Value",
    ItemsSource = new ViewModel().Data1,
    GroupingLabel="GroupTwo"
};
StackingColumnSeries  series = new  StackingColumnSeries()
{
    XBindingPath = "Name",
    YBindingPath = "Value",
    ItemsSource = new ViewModel().Data2,
    GroupingLabel="GroupOne"
};

chart.Series.Add(series);
chart.Series.Add(series1);     
this.Content = chart;

{% endhighlight %}

{% endtabs %}

![Grouping label in MAUI Chart]()

## Appearance customization

* [Spacing]() of the `Double` type is used to change the spacing between two segments. The default spacing value is 0, ranging from 0 to 1.
* [Width]() of the `Double` type is used to change the width of the rectangle. The default value of the width is 0.8, and the value ranges from 0 to 1.
* [CornerRadius]() of the type `CornerRadius`, indicates the rounded corner for the stacked column.
* [Stroke]() of the type `Brush` indicates the brush used to paint the border of the stacked column.
* [StrokeWidth]() of the type `Double` indicates the width of the stacked segment.