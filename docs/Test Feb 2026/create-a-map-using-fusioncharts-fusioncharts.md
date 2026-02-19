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

<Tabs>
  <Tab title="NPM">
    **To install the `fusioncharts` package via npm run the command below:**

    ```powershell
    npm install fusioncharts
    ```
  </Tab>
  <Tab title="CDN">
    **To install the FusionCharts Suite follow the steps below:**

    1. Include the **FusionCharts** JavaScript files from CDN.
    2. Include the FusionCharts map renderer.
    3. Include the map definition file.
    4. Include the FusionCharts theme file to apply style to the charts.

    The code is shown below:

    ```html
    <head>
        <!-- Step 1 - Include the fusioncharts core library -->
        <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.js"></script>
        <!-- Step 2 - Include the map renderer file -->
        <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.maps.js"></script>
        <!-- Step 3 - Include the map definition file -->
        <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.world.js"></script>
        <!-- Step 4 - Include the fusion theme -->
        <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/themes/fusioncharts.theme.fusion.js"></script>
    </head>
    ```
  </Tab>
  <Tab title="Local Files">
    **To install the FusionCharts Suite follow the steps below:**

    1. Include the **FusionCharts** JavaScript files, which can be downloaded from [here](https://www.fusioncharts.com/download/fusioncharts-suite-xt).
    2. Include the FusionCharts map renderer.
    3. Include the map definition file.
    4. Include the FusionCharts theme file to apply style to the charts.

    The code is shown below:

    ```html
    <head>
        <!-- Step 1 - Include the fusioncharts core library -->
        <script type="text/javascript" src="path/to/local/fusioncharts.js"></script>
        <!-- Step 2 - Include the map renderer file -->
        <script type="text/javascript" src="path/to/local/fusioncharts.maps.js"></script>
        <!-- Step 3 - Include the map definition file -->
        <script type="text/javascript" src="path/to/local/fusioncharts.world.js"></script>
        <!-- Step 4 - Include the fusion theme -->
        <script type="text/javascript" src="path/to/local/themes/fusioncharts.theme.fusion.js"></script>
    </head>
    ```
  </Tab>
</Tabs>