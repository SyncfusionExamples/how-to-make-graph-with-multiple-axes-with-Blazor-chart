# Multiple Y-Axes in Syncfusion Blazor Chart

## Overview

This sample demonstrates how to configure multiple Y-axes in a Syncfusion [Blazor Charts](https://www.syncfusion.com/blazor-components/blazor-charts) component. The implementation adds a secondary axis through the `ChartAxes` collection and maps an individual series to that axis using the `YAxisName` property.

This approach is useful when multiple datasets must be displayed within the same chart area while maintaining separate axis scales. The sample uses two spline series and a DateTime-based X-axis to illustrate axis-to-series mapping.

## Key Features

- Uses the `SfChart` component to render chart data.
- Configures a DateTime X-axis through `ChartPrimaryXAxis`.
- Defines the default Y-axis with `ChartPrimaryYAxis`.
- Adds a secondary Y-axis using the `ChartAxes` collection.
- Configures a secondary `ChartAxis` with:
  - `Name="YAxis"`
  - `OpposedPosition="true"`
  - `Interval`
  - `Minimum`
  - `Maximum`
- Renders two spline series using `ChartSeries`.
- Binds data through the `DataSource` property.
- Maps data fields through:
  - `XName`
  - `YName`
- Associates a series with the secondary Y-axis through the `YAxisName` property.
- Removes major and minor gridlines using:
  - `ChartAxisMajorGridLines`
  - `ChartAxisMinorGridLines`

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download the repository.
2. Open the project file:
   `MultipleAxisInBlazorChart/MultipleAxisInBlazorChart.csproj`
3. Restore NuGet packages.
4. Build the project.
5. Run the application using `Ctrl+F5`.

**Visual Studio Code**

1. Clone or download the repository.
2. Open the repository folder in Visual Studio Code.
3. Open the integrated terminal.
4. Navigate to the project folder.

```bash
cd MultipleAxisInBlazorChart
```

5. Restore NuGet packages:

```bash
dotnet restore
```

6. Run the application:

```bash
dotnet run
```

7. Open the local URL displayed in the console output.

## Project Structure

`MultipleAxisInBlazorChart/Pages/Index.razor` - Implements the multiple-axis chart sample using `SfChart`, `ChartAxes`, `ChartAxis`, and `ChartSeries`.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Refer to the official Syncfusion Chart documentation: https://help.syncfusion.com/chart-sdk/blazor/charts/getting-started

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.