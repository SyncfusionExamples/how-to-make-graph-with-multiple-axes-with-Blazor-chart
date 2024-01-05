# How-to-make-graph-with-multiple-axes-with-Blazor-chart

This article explains how to add multiple Y axis in [Blazor Chart](https://www.syncfusion.com/blazor-components/blazor-charts) . 

**Blazor chart with multiple Y axis**

Blazor chart provide a support to use multiple axis at a time by using [ChartAxes](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartAxes.html).

The [ChartAxes](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartAxes.html) is a secondary axis collection that can be used to add “n” number of axes to the chart in addition to the basic X and Y axis. By mapping with the axis unique name, series can be linked to it.

In the below code example, the series and axis are linked together by using [Name](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartAxis.html#Syncfusion_Blazor_Charts_ChartAxis_Name) property of [ChartAxis](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartAxis.html) by providing same name for [YAxisName](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartSeries.html#Syncfusion_Blazor_Charts_ChartSeries_YAxisName) property. 

```cshtml

<ChartAxes> <ChartAxis Name="YAxis" OpposedPosition="true"/></ChartAxes>
 <ChartSeriesCollection>
    <ChartSeries DataSource="@WeatherReports" XName="Month" YName="Product1" Type="ChartSeriesType.Spline" Fill="blue">
    </ChartSeries>
    <ChartSeries DataSource="@WeatherReports" XName="Month" YName="Product2" Type="ChartSeriesType.Spline" Fill="pink" YAxisName="YAxis">
    </ChartSeries>
</ChartSeriesCollection>

```

The following code snippet illustrates the how to create graph with multiple Y axis.

**Index.razor**

```cshtml

@using Syncfusion.Blazor.Charts

<SfChart>

    <ChartPrimaryXAxis ValueType="Syncfusion.Blazor.Charts.ValueType.DateTime" Interval="1" IntervalType="IntervalType.Months">
        <ChartAxisMajorGridLines Width="0"/>
        <ChartAxisMinorGridLines Width="0"/>
    </ChartPrimaryXAxis>

    <ChartPrimaryYAxis>
        <ChartAxisMajorGridLines Width="0"/>
        <ChartAxisMinorGridLines Width="0"/>
    </ChartPrimaryYAxis>

    <ChartAxes>
        <ChartAxis Name="YAxis" OpposedPosition="true" Interval="10" Minimum="10" Maximum="50"/>
    </ChartAxes>

    <ChartSeriesCollection>
        <ChartSeries DataSource="@WeatherReports" XName="Month" YName="Product1" Type="ChartSeriesType.Spline" Fill="blue">
        </ChartSeries>
        <ChartSeries DataSource="@WeatherReports" XName="Month" YName="Product2" Type="ChartSeriesType.Spline" Fill="pink" YAxisName="YAxis">
        </ChartSeries>
    </ChartSeriesCollection>

</SfChart>

@code {

    public class Chart
    {
        public DateTime Month { get; set; }
        public double Product1 { get; set; }
        public double Product2 { get; set; }
    }

    public List<Chart> WeatherReports = new List<Chart>
    {
        new Chart { Month = new DateTime(2005, 01, 01), Product1 = 21, Product2 = 26 },
        new Chart { Month = new DateTime(2005, 02, 01), Product1 = 24, Product2 = 20 },
        new Chart { Month = new DateTime(2005, 03, 01), Product1 = 36, Product2 = 30 },
        new Chart { Month = new DateTime(2005, 04, 01), Product1 = 30, Product2 = 40 },
        new Chart { Month = new DateTime(2005, 05, 01), Product1 = 25, Product2 = 35 },
        new Chart { Month = new DateTime(2005, 06, 01), Product1 = 20, Product2 = 30 },
        new Chart { Month = new DateTime(2005, 07, 01), Product1 = 40, Product2 = 20 },
        new Chart { Month = new DateTime(2005, 08, 01), Product1 = 35, Product2 = 45 },
    };
}

```

The following screenshot illustrates the output of the above code snippet.

**Output:**

![](/blazor-chart-with-multiple-y-axis.png)

**Conclusion**

I hope you enjoyed learning how to add multiple Y axis in Blazor Chart Component.

You can refer to our [Blazor Chart feature tour](https://www.syncfusion.com/blazor-components/blazor-charts) page to know about its other groundbreaking feature representations and [documentation](https://blazor.syncfusion.com/documentation/chart/getting-started), and how to quickly get started for configuration specifications. You can also explore our [Blazor Chart example](https://blazor.syncfusion.com/demos/chart/line?theme=bootstrap5) to understand how to create and manipulate data.

For current customers, you can check out our components from the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/blazor) to check out our other controls.

If you have any queries or require clarifications, please let us know in the comments section below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [support portal](https://support.syncfusion.com/create), or [feedback portal](https://www.syncfusion.com/feedback/blazor-components?control=charts). We are always happy to assist you!