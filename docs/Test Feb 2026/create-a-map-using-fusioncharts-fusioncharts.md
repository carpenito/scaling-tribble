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

| State | Entity Name | Value |
| ----- | ----------- | ----- ||
| North America | NA | 82 |
| South America | SA | 2.04 |
| Asia | AS | 1.78 |
| Europe | EU | 40 |
| Africa | AF | 2.58 |
| Australia | AU | 1.30 |

In the above table, the column **Entity Name** represents the geographical entities represented in the map, whose full names are given in the **State** column.

FusionCharts accepts data in **JSON** format in which the above entities are denoted by the `id` key in the `data` object.

For any map visualization, it is important to provide the correct value for the `id` keys. For example, if you want to denote Africa, the value for the corresponding `id` must be `AF` and not `AFR`.

We have a detailed [Map Specification Sheets](https://www.fusioncharts.com/dev/maps/spec-sheets/world) for all the maps that can be rendered using FusionCharts, where you can find the correct `id` of the maps you want to create.

Following code is the JSON representation of the above table with the required attributes to render the above map.
