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

[INSERT MAP]

## Map Data

The data for the above map is represented in the table below:

| State         | Entity Name | Value |
| ------------- | ----------- | ----- |
| North America | NA          | 82    |
| South America | SA          | 2.04  |
| Asia          | AS          | 1.78  |
| Europe        | EU          | 40    |
| Africa        | AF          | 2.58  |
| Australia     | AU          | 1.30  |

In the above table, the column **Entity Name** represents the geographical entities represented in the map, whose full names are given in the **State** column.

FusionCharts accepts data in **JSON** format in which the above entities are denoted by the `id` key in the `data` object.

For any map visualization, it is important to provide the correct value for the `id` keys. For example, if you want to denote Africa, the value for the corresponding `id` must be `AF` and not `AFR`.

We have a detailed [Map Specification Sheets](https://www.fusioncharts.com/dev/maps/spec-sheets/world) for all the maps that can be rendered using FusionCharts, where you can find the correct `id` of the maps you want to create.

Following code is the JSON representation of the above table with the required attributes to render the above map.

```json
{
    // Map Configuration
    "chart": {
            "caption": "Average Annual Population Growth",
            "subcaption": " 1955-2015",
            "numbersuffix": "%",
            "includevalueinlabels": "1",
            "labelsepchar": ": ",
            "entityFillHoverColor": "#FFF9C4",
            "theme": "fusion"
    },
    // Aesthetics; ranges synced with the slider
    "colorrange": {
        "minvalue": "0",
        "code": "#FFE0B2",
        "gradient": "1",
        "color": [{
            "minvalue": "0.5",
            "maxvalue": "1.0",
            "color": "#FFD74D"
        }, {
            "minvalue": "1.0",
            "maxvalue": "2.0",
            "color": "#FB8C00"
        }, {
            "minvalue": "2.0",
            "maxvalue": "3.0",
            "color": "#E65100"
        }]
    },
    // Source data as JSON --> id represents countries of world.
    "data": [{
        "id": "NA",
        "value": ".82",
        "showLabel": "1"
    }, {
        "id": "SA",
        "value": "2.04",
        "showLabel": "1"
    }, {
        "id": "AS",
        "value": "1.78",
        "showLabel": "1"
    }, {
        "id": "EU",
        "value": ".40",
        "showLabel": "1"
    }, {
        "id": "AF",
        "value": "2.58",
        "showLabel": "1"
    }, {
        "id": "AU",
        "value": "1.30",
        "showLabel": "1"
    }]
}
```

In the above JSON data:

* Create the `chart` object to define the elements of the map.

* Create the `colorRange` array to set the color associated with the specific range of values.

* Specify `minValue` and `maxValue` within the `color` array under the `colorRange` array.

* Create the `data` array to define the id of the continents and their corresponding values along with configurations. For example, the first object under `data` array contains the `id` and `value` of **North America** as **NA** and **.82** respectively.

The chart object and the respective arrays contain a set of key-value pairs known as **attributes**. These attributes are used to set the functional and cosmetic properties of the map.

Now that you have the data in JSON format, let's render the map.

## Render the Map

To render the map follow the steps below:

1. Include the `fusioncharts` library.

2. Include the FusionMaps renderer.

3. Include the map definition file.

4. Include the FusionCharts theme file to apply style to the charts.

5. Add the map renderer and map definition as a dependency to the core.

6. Add the theme as a dependency to the core.

7. Store the chart configurations as a JSON object. In this JSON object:

   * Set the map type as `world`. Each map is represented with a unique map alias. For World map, the alias is `world`. Find the complete list of map types with their respective alias [here](https://www.fusioncharts.com/dev/map-guide/list-of-maps).

   * Set the width and height (in pixels).

   * Set the `dataFormat` as **json**.

   * Embed the json data as the value of the `dataSource`.

8. Add a container (instance) for the chart.

The consolidated code is shown below:

<Tabs>
  <Tab title="NPM">
    **The`fusioncharts` package for `npm` can be used in two different ways:**

    * FusionCharts ES module
    * FusionCharts CJS module

    **The steps to render a map for both modules are shown below:**

    #### ES6

    ```javascript
    // Include the core fusioncharts file from core
    import FusionCharts from 'fusioncharts/core';

    // Include the map files
    import FusionMaps from 'fusioncharts/maps';
    import World from 'fusioncharts/maps/es/fusioncharts.world';

    // Include the fusion theme
    import FusionTheme from 'fusioncharts/themes/es/fusioncharts.theme.fusion'

    // Add the map and theme as dependency
    FusionCharts.addDep(FusionMaps);
    FusionCharts.addDep(World);
    FusionCharts.addDep(FusionTheme);

    // Create an Instance with map options
    var annualPopulation = new FusionCharts({
        type: 'world',
        width: '800',
        height: '550',
        dataFormat: 'json',
        renderAt: 'chart-container',
        dataSource: {
            "chart": {
                "caption": "Average Annual Population Growth",
                "subcaption": " 1955-2015",
                "numbersuffix": "%",
                "includevalueinlabels": "1",
                "labelsepchar": ": ",
                "entityFillHoverColor": "#FFF9C4",
                "theme": "fusion"
            },
            "colorrange": {
                "minvalue": "0",
                "code": "#FFE0B2",
                "gradient": "1",
                "color": [{
                    "minvalue": "0.5",
                    "maxvalue": "1.0",
                    "color": "#FFD74D"
                }, {
                    "minvalue": "1.0",
                    "maxvalue": "2.0",
                    "color": "#FB8C00"
                }, {
                    "minvalue": "2.0",
                    "maxvalue": "3.0",
                    "color": "#E65100"
                }]
            },
            "data": [{
                "id": "NA",
                "value": ".82",
                "showLabel": "1"
            }, {
                "id": "SA",
                "value": "2.04",
                "showLabel": "1"
            }, {
                "id": "AS",
                "value": "1.78",
                "showLabel": "1"
            }, {
                "id": "EU",
                "value": ".40",
                "showLabel": "1"
            }, {
                "id": "AF",
                "value": "2.58",
                "showLabel": "1"
            }, {
                "id": "AU",
                "value": "1.30",
                "showLabel": "1"
            }]
        }
    });
    // Render
    annualPopulation.render();
    ```

    #### CJS

    ```javascript
    var FusionCharts = require('fusioncharts');

    // Require maps from fusioncharts
    var FusionMaps = require('fusioncharts/fusioncharts.maps');
    var World = require('fusioncharts/maps/fusioncharts.world');

    // Require theme from fusioncharts
    var FusionTheme = require('fusioncharts/themes/fusioncharts.theme.fusion');

    // Add maps and themes as dependency
    FusionMaps(FusionCharts);
    World(FusionCharts);
    FusionTheme(FusionCharts);

    // Create an Instance with map options
    var annualPopulation = new FusionCharts({
        type: 'world',
        width: '800',
        height: '550',
        dataFormat: 'json',
        renderAt: 'chart-container',
        dataSource: {
            "chart": {
                "caption": "Average Annual Population Growth",
                "subcaption": " 1955-2015",
                "numbersuffix": "%",
                "includevalueinlabels": "1",
                "labelsepchar": ": ",
                "entityFillHoverColor": "#FFF9C4",
                "theme": "fusion"
            },
            "colorrange": {
                "minvalue": "0",
                "code": "#FFE0B2",
                "gradient": "1",
                "color": [{
                    "minvalue": "0.5",
                    "maxvalue": "1.0",
                    "color": "#FFD74D"
                }, {
                    "minvalue": "1.0",
                    "maxvalue": "2.0",
                    "color": "#FB8C00"
                }, {
                    "minvalue": "2.0",
                    "maxvalue": "3.0",
                    "color": "#E65100"
                }]
            },
            "data": [{
                "id": "NA",
                "value": ".82",
                "showLabel": "1"
            }, {
                "id": "SA",
                "value": "2.04",
                "showLabel": "1"
            }, {
                "id": "AS",
                "value": "1.78",
                "showLabel": "1"
            }, {
                "id": "EU",
                "value": ".40",
                "showLabel": "1"
            }, {
                "id": "AF",
                "value": "2.58",
                "showLabel": "1"
            }, {
                "id": "AU",
                "value": "1.30",
                "showLabel": "1"
            }]
        }
    });
    // Render
    annualPopulation.render();
    ```
  </Tab>

  <Tab title="CDN">
    ```html
    <html>
    <head>
        <title>My First map using FusionCharts Suite XT</title>
        <!-- Including the fusioncharts core library -->
        <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.js"></script>
        <!-- Including the map renderer file -->
        <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.maps.js"></script>
        <!-- Including the map definition file -->
        <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.world.js"></script>
        <!-- Including the fusion theme -->
        <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/themes/fusioncharts.theme.fusion.js"></script>
        <script type="text/javascript">
            FusionCharts.ready(function() {
                var annualPopulation = new FusionCharts({
                    "type": "maps/world",
                    "renderAt": "chart-container",
                    "width": "800",
                    "height": "550",
                    "dataFormat": "json",
                    "dataSource": {
                        "chart": {
                            "caption": "Average Annual Population Growth",
                            "subcaption": " 1955-2015",
                            "numbersuffix": "%",
                            "includevalueinlabels": "1",
                            "labelsepchar": ": ",
                            "entityFillHoverColor": "#FFF9C4",
                            "theme": "fusion"
                        },
                        "colorrange": {
                            "minvalue": "0",
                            "code": "#FFE0B2",
                            "gradient": "1",
                            "color": [{
                                "minvalue": "0.5",
                                "maxvalue": "1.0",
                                "color": "#FFD74D"
                            }, {
                                "minvalue": "1.0",
                                "maxvalue": "2.0",
                                "color": "#FB8C00"
                            }, {
                                "minvalue": "2.0",
                                "maxvalue": "3.0",
                                "color": "#E65100"
                            }]
                        },
                        "data": [{
                            "id": "NA",
                            "value": ".82",
                            "showLabel": "1"
                        }, {
                            "id": "SA",
                            "value": "2.04",
                            "showLabel": "1"
                        }, {
                            "id": "AS",
                            "value": "1.78",
                            "showLabel": "1"
                        }, {
                            "id": "EU",
                            "value": ".40",
                            "showLabel": "1"
                        }, {
                            "id": "AF",
                            "value": "2.58",
                            "showLabel": "1"
                        }, {
                            "id": "AU",
                            "value": "1.30",
                            "showLabel": "1"
                        }]
                    }
                });
                annualPopulation.render();
            });
        </script>
    </head>
    <body>
        <div id="chart-container">FusionMaps XT will load map here!</div>
    </body>
    </html>
    ```
  </Tab>

  <Tab title="Local Files">
    ```html
    <html>
    <head>
        <title>My First map using FusionCharts Suite XT</title>
        <!-- Including the fusioncharts core library -->
        <script type="text/javascript" src="path/to/local/fusioncharts.js"></script>
        <!-- Including the map renderer file -->
        <script type="text/javascript" src="path/to/local/fusioncharts.maps.js"></script>
        <!-- Including the map definition file -->
        <script type="text/javascript" src="path/to/local/fusioncharts.world.js"></script>
        <!-- Including the fusion theme -->
        <script type="text/javascript" src="path/to/local/themes/fusioncharts.theme.fusion.js"></script>
        <script type="text/javascript">
            FusionCharts.ready(function() {
                var annualPopulation = new FusionCharts({
                    "type": "maps/world",
                    "renderAt": "chart-container",
                    "width": "800",
                    "height": "550",
                    "dataFormat": "json",
                    "dataSource": {
                        "chart": {
                            "caption": "Average Annual Population Growth",
                            "subcaption": " 1955-2015",
                            "numbersuffix": "%",
                            "includevalueinlabels": "1",
                            "labelsepchar": ": ",
                            "entityFillHoverColor": "#FFF9C4",
                            "theme": "fusion"
                        },
                        "colorrange": {
                            "minvalue": "0",
                            "code": "#FFE0B2",
                            "gradient": "1",
                            "color": [{
                                "minvalue": "0.5",
                                "maxvalue": "1.0",
                                "color": "#FFD74D"
                            }, {
                                "minvalue": "1.0",
                                "maxvalue": "2.0",
                                "color": "#FB8C00"
                            }, {
                                "minvalue": "2.0",
                                "maxvalue": "3.0",
                                "color": "#E65100"
                            }]
                        },
                        "data": [{
                            "id": "NA",
                            "value": ".82",
                            "showLabel": "1"
                        }, {
                            "id": "SA",
                            "value": "2.04",
                            "showLabel": "1"
                        }, {
                            "id": "AS",
                            "value": "1.78",
                            "showLabel": "1"
                        }, {
                            "id": "EU",
                            "value": ".40",
                            "showLabel": "1"
                        }, {
                            "id": "AF",
                            "value": "2.58",
                            "showLabel": "1"
                        }, {
                            "id": "AU",
                            "value": "1.30",
                            "showLabel": "1"
                        }]
                    }
                });
                annualPopulation.render();
            });
        </script>
    </head>
    <body>
        <div id="chart-container">FusionMaps XT will load map here!</div>
    </body>
    </html>
    ```
  </Tab>
</Tabs>

That's it! Your first map using Plain JavaScript is ready.

## Render other maps

To reduce the size of the package FusionCharts comes with only two maps, i.e., the **World** map and the **USA** map. However, FusionCharts provide 1600+ maps for you to explore. [Download](https://www.fusioncharts.com/download/map-definition-files) the map files separately if you want to save them locally.

Let's create a map of California to show the "Web visits for a particular month" as shown below:
