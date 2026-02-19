---
title: Create a Map Using FusionCharts | FusionCharts
excerpt: >-
  This article outlines the steps to be executed for creating your first map
  using the plain javascript. heading: Create a Map Using FusionCharts
deprecated: false
hidden: false
icon: fad fa-rocket-launch
metadata:
  robots: index
---
**FusionCharts Suite XT** — the industry's most comprehensive JavaScript charting solution — is all about easing the whole process of data visualization through charts.

In this page, we'll see how to install **FusionCharts** library and all the other dependencies on your system and render a map using Plain JavaScript.

## Installation

Install **FusionCharts** using any of the following steps:

<FusionChartInstallation />

That completes the installation of **FusionCharts** Suite.

## Create Your First Map

In this section, we will create a visualization using the **World Map** showing the average annual population growth.

The chart data uses geographical entity IDs (e.g., `NA` for North America, `AF` for Africa) and a color gradient to represent growth ranges.

<HTMLBlock>{`
<div id="chart-container" style="width:100%;max-width:800px;margin:0 auto;"></div>
<script src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.js"></script>
<script src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.maps.js"></script>
<script src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.world.js"></script>
<script src="https://cdn.fusioncharts.com/fusioncharts/latest/themes/fusioncharts.theme.fusion.js"></script>
<script>
FusionCharts.ready(function() {
    var mapObj = new FusionCharts({
        type: "maps/world",
        renderAt: "chart-container",
        width: "100%",
        height: "550",
        dataFormat: "json",
        dataSource: {
            chart: {
                caption: "Average Annual Population Growth",
                subcaption: "1955-2015",
                numbersuffix: "%",
                includevalueinlabels: "1",
                labelsepchar: ": ",
                entityFillHoverColor: "#FFF9C4",
                theme: "fusion"
            },
            colorrange: {
                minvalue: "0",
                code: "#FFE0B2",
                gradient: "1",
                color: [
                    { minvalue: "0.5", maxvalue: "1.0", color: "#FFD74D" },
                    { minvalue: "1.0", maxvalue: "2.0", color: "#FB8C00" },
                    { minvalue: "2.0", maxvalue: "3.0", color: "#E65100" }
                ]
            },
            data: [
                { id: "NA", value: ".82", showLabel: "1" },
                { id: "SA", value: "2.04", showLabel: "1" },
                { id: "AS", value: "1.78", showLabel: "1" },
                { id: "EU", value: ".40", showLabel: "1" },
                { id: "AF", value: "2.58", showLabel: "1" },
                { id: "AU", value: "1.30", showLabel: "1" }
            ]
        }
    });
    mapObj.render();
});
</script>
`}</HTMLBlock>

```html title="getting-started-your-first-map.html"
<html>
<head>
    <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.js"></script>
    <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.maps.js"></script>
    <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.world.js"></script>
    <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/themes/fusioncharts.theme.fusion.js"></script>
</head>
<body>
    <div id="chart-container">A world map will load here!</div>
    <script type="text/javascript">
        FusionCharts.ready(function() {
            var mapObj = new FusionCharts({
                type: "maps/world",
                renderAt: "chart-container",
                width: "800",
                height: "550",
                dataFormat: "json",
                dataSource: {
                    chart: {
                        caption: "Average Annual Population Growth",
                        subcaption: "1955-2015",
                        numbersuffix: "%",
                        includevalueinlabels: "1",
                        labelsepchar: ": ",
                        entityFillHoverColor: "#FFF9C4",
                        theme: "fusion"
                    },
                    colorrange: {
                        minvalue: "0",
                        code: "#FFE0B2",
                        gradient: "1",
                        color: [
                            { minvalue: "0.5", maxvalue: "1.0", color: "#FFD74D" },
                            { minvalue: "1.0", maxvalue: "2.0", color: "#FB8C00" },
                            { minvalue: "2.0", maxvalue: "3.0", color: "#E65100" }
                        ]
                    },
                    data: [
                        { id: "NA", value: ".82", showLabel: "1" },
                        { id: "SA", value: "2.04", showLabel: "1" },
                        { id: "AS", value: "1.78", showLabel: "1" },
                        { id: "EU", value: ".40", showLabel: "1" },
                        { id: "AF", value: "2.58", showLabel: "1" },
                        { id: "AU", value: "1.30", showLabel: "1" }
                    ]
                }
            });
            mapObj.render();
        });
    </script>
</body>
</html>
```

When you open this HTML file in a browser, the map renders a color-coded world map where each continent is shaded based on its population growth rate:

| Color | Growth Range | Example |
|---|---|---|
| `#FFD74D` (yellow) | 0.5% – 1.0% | North America (0.82%) |
| `#FB8C00` (orange) | 1.0% – 2.0% | Asia (1.78%) |
| `#E65100` (deep orange) | 2.0% – 3.0% | Africa (2.58%) |