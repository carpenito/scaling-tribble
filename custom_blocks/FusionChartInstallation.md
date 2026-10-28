---
name: FusionChartInstallation
---
<Tabs>
  <Tab title="NPM">
    **Para instalar el paquete `fusioncharts` mediante npm, ejecuta el siguiente comando:**

    ```powershell
    npm install fusioncharts
    ```
  </Tab>

  <Tab title="CDN">
    **Para instalar FusionCharts Suite, sigue los pasos a continuación:**

    1. Incluye los archivos JavaScript de **FusionCharts** desde la CDN.
    2. Incluye el renderizador de mapas de FusionCharts.
    3. Incluye el archivo de definición del mapa.
    4. Incluye el archivo de temas de FusionCharts para aplicar estilo a los gráficos.

    El código se muestra a continuación:

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

  <Tab title="Archivos locales">
    **Para instalar FusionCharts Suite, sigue los pasos a continuación:**

    1. Incluye los archivos JavaScript de **FusionCharts**, que se pueden descargar desde [aquí](https://www.fusioncharts.com/download/fusioncharts-suite-xt).
    2. Incluye el renderizador de mapas de FusionCharts.
    3. Incluye el archivo de definición del mapa.
    4. Incluye el archivo de temas de FusionCharts para aplicar estilo a los gráficos.

    El código se muestra a continuación:

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
