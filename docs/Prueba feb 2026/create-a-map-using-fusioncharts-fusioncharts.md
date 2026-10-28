---
title: Crear un mapa usando FusionCharts | FusionCharts
excerpt: >-
  Este artículo describe los pasos a seguir para crear su primer mapa utilizando
  JavaScript puro. encabezado: Crear un mapa usando FusionCharts
deprecated: false
hidden: false
icon: fad fa-rocket-launch
metadata:
  robots: index
---
**FusionCharts Suite XT** —la solución de gráficos JavaScript más completa de la industria— tiene como objetivo facilitar todo el proceso de visualización de datos mediante gráficos.

En esta página, veremos cómo instalar la biblioteca **FusionCharts** y todas las demás dependencias en su sistema y renderizar un mapa utilizando JavaScript puro.

## Instalación {#installation}

Instale **FusionCharts** siguiendo cualquiera de los siguientes pasos:

<Tabs>
  <Tab title="NPM">
    **Para instalar el paquete `fusioncharts` a través de npm, ejecute el siguiente comando:**

    ```powershell
    npm install fusioncharts
    ```
  </Tab>

  <Tab title="CDN">
    **Para instalar FusionCharts Suite, siga los pasos a continuación:**

    1. Incluya los archivos JavaScript de **FusionCharts** desde la CDN.
    2. Incluya el renderizador de mapas de FusionCharts.
    3. Incluya el archivo de definición del mapa.
    4. Incluya el archivo de tema de FusionCharts para aplicar estilo a los gráficos.

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
    **Para instalar FusionCharts Suite, siga los pasos a continuación:**

    1. Incluya los archivos JavaScript de **FusionCharts**, que se pueden descargar desde [aquí](https://www.fusioncharts.com/download/fusioncharts-suite-xt).
    2. Incluya el renderizador de mapas de FusionCharts.
    3. Incluya el archivo de definición del mapa.
    4. Incluya el archivo de tema de FusionCharts para aplicar estilo a los gráficos.

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

Esto completa la instalación de **FusionCharts** Suite.

## Cree su primer mapa {#create-your-first-map}

En esta sección, crearemos una visualización utilizando el **mapa mundial** que muestra el crecimiento promedio anual de la población.

Los datos del gráfico utilizan identificadores de entidades geográficas (por ejemplo, `NA` para América del Norte, `AF` para África) y un degradado de color para representar rangos de crecimiento.

<RemoteFusionChartsMap configUrl="https://raw.githubusercontent.com/aerdman1/aerdman1.github.io/refs/heads/main/fusioncharts-map-world.json" height={550} />

## Datos del mapa {#map-data}

Los datos para el mapa anterior se representan en la siguiente tabla:

| Estado            | Nombre de la entidad | Valor |
| ----------------- | -------------------- | ----- |
| América del Norte | NA                   | 82    |
| América del Sur   | SA                   | 2.04  |
| Asia              | AS                   | 1.78  |
| Europa            | EU                   | 40    |
| África            | AF                   | 2.58  |
| Australia         | AU                   | 1.30  |

En la tabla anterior, la columna **Nombre de la entidad** representa las entidades geográficas representadas en el mapa, cuyos nombres completos se indican en la columna **Estado**.

FusionCharts acepta datos en formato **JSON** en el que las entidades anteriores se indican mediante la clave `id` en el objeto `data`.

Para cualquier visualización de mapas, es importante proporcionar el valor correcto para las claves `id`. Por ejemplo, si desea indicar África, el valor del `id` correspondiente debe ser `AF` y no `AFR`.

Disponemos de [hojas de especificaciones de mapas](https://www.fusioncharts.com/dev/maps/spec-sheets/world) detalladas para todos los mapas que se pueden renderizar con FusionCharts, donde puede encontrar el `id` correcto de los mapas que desea crear.

El siguiente código es la representación JSON de la tabla anterior con los atributos requeridos para renderizar el mapa anterior.

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

En los datos JSON anteriores:

- Cree el objeto `chart` para definir los elementos del mapa.

- Cree el array `colorRange` para definir el color asociado al rango específico de valores.

- Especifique `minValue` y `maxValue` dentro del array `color` bajo el array `colorRange`.

- Cree el array `data` para definir el id de los continentes y sus valores correspondientes junto con las configuraciones. Por ejemplo, el primer objeto dentro del array `data` contiene el `id` y el `value` de **América del Norte** como **NA** y **.82**, respectivamente.

El objeto chart y los respectivos arrays contienen un conjunto de pares clave-valor conocidos como **atributos**. Estos atributos se utilizan para definir las propiedades funcionales y estéticas del mapa.

Ahora que tiene los datos en formato JSON, vamos a renderizar el mapa.

## Renderizar el mapa {#render-the-map}

Para renderizar el mapa, siga los pasos a continuación:

1. Incluya la biblioteca `fusioncharts`.

2. Incluya el renderizador de FusionMaps.

3. Incluya el archivo de definición del mapa.

4. Incluya el archivo de tema de FusionCharts para aplicar estilo a los gráficos.

5. Añada el renderizador del mapa y la definición del mapa como una dependencia al núcleo.

6. Añada el tema como una dependencia al núcleo.

7. Almacene las configuraciones del gráfico como un objeto JSON. En este objeto JSON:

   - Establezca el tipo de mapa como `world`. Cada mapa se representa con un alias de mapa único. Para el mapa del mundo, el alias es `world`. Encuentre la lista completa de tipos de mapas con sus respectivos alias [aquí](https://www.fusioncharts.com/dev/map-guide/list-of-maps).

   - Establezca el ancho y el alto (en píxeles).

   - Establezca `dataFormat` como **json**.

   - Incruste los datos json como el valor de `dataSource`.

8. Añada un contenedor (instancia) para el gráfico.

El código consolidado se muestra a continuación:

<Tabs>
  <Tab title="NPM">
    **El paquete `fusioncharts` para `npm` se puede utilizar de dos formas diferentes:**

    - Módulo ES de FusionCharts
    - Módulo CJS de FusionCharts

    **Los pasos para renderizar un mapa para ambos módulos se muestran a continuación:**

    #### ES6 {#es6}

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

    #### CJS {#cjs}

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

  <Tab title="Archivos locales">
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

¡Eso es todo! Su primer mapa con JavaScript puro está listo.

## Renderizar otros mapas {#render-other-maps}

Para reducir el tamaño del paquete, FusionCharts incluye solo dos mapas, es decir, el mapa del **Mundo** y el mapa de **EE. UU.** Sin embargo, FusionCharts ofrece más de 1600 mapas para que los explore. [Descargue](https://www.fusioncharts.com/download/map-definition-files) los archivos de mapas por separado si desea guardarlos localmente.

Vamos a crear un mapa de California para mostrar las "Visitas web de un mes determinado", como se muestra a continuación:

<Tabs>
  <Tab title="GRÁFICO">
    <FusionCaliMap configUrl="https://raw.githubusercontent.com/carpenito/kirb-translationsQA2025/refs/heads/v1.0/fusioncharts.california.js" height={550} fcVersion="4.2.1" />

    Para renderizar el mapa anterior, primero instale el paquete fusionmaps, que contiene todos los archivos de definición de mapas, como se muestra a continuación:

    ```
    $ npm install fusionmaps
    ```
  </Tab>

  <Tab title="JSON">
    ```
    {
    "chart": {
        "animation": "0",
        "showbevel": "0",
        "usehovercolor": "1",
        "showlegend": "1",
        "legendposition": "BOTTOM",
        "legendborderalpha": "0",
        "legendbordercolor": "ffffff",
        "legendallowdrag": "0",
        "caption": "Website Visits for the month of March 2018",
        "connectorcolor": "000000",
        "fillalpha": "80",
        "hovercolor": "CCCCCC",
        "theme": "fusion"
    },
    "colorrange": {
        "minvalue": "0",
        "startlabel": "Low",
        "endlabel": "High",
        "code": "e44a00",
        "gradient": "1",
        "color": [
            {
                "maxvalue": "2500",
                "code": "f8bd19"
            },
            {
                "maxvalue": "5000",
                "code": "6baa01"
            }
        ]
    },
    "data": [
        {
            "id": "001",
            "value": 2834
        },
        {
            "id": "003",
            "value": 3182
        },
        {
            "id": "005",
            "value": 3280
        },
        {
            "id": "007",
            "value": 911
        },
        {
            "id": "009",
            "value": 292
        },
        {
            "id": "011",
            "value": 530
        },
        {
            "id": "013",
            "value": 2515
        },
        {
            "id": "015",
            "value": 728
        },
        {
            "id": "017",
            "value": 1974
        },
        {
            "id": "019",
            "value": 848
        },
        {
            "id": "021",
            "value": 3278
        },
        {
            "id": "023",
            "value": 4463
        },
        {
            "id": "025",
            "value": 1198
        },
        {
            "id": "027",
            "value": 378
        },
        {
            "id": "029",
            "value": 2610
        },
        {
            "id": "031",
            "value": 1200
        },
        {
            "id": "033",
            "value": 3820
        },
        {
            "id": "035",
            "value": 940
        },
        {
            "id": "037",
            "value": 3416
        },
        {
            "id": "039",
            "value": 4004
        },
        {
            "id": "041",
            "value": 1604
        },
        {
            "id": "043",
            "value": 4011
        },
        {
            "id": "045",
            "value": 3203
        },
        {
            "id": "047",
            "value": 3775
        },
        {
            "id": "049",
            "value": 2721
        },
        {
            "id": "051",
            "value": 3417
        },
        {
            "id": "053",
            "value": 1530
        },
        {
            "id": "055",
            "value": 412
        },
        {
            "id": "057",
            "value": 3434
        },
        {
            "id": "059",
            "value": 1670
        },
        {
            "id": "061",
            "value": 1274
        },
        {
            "id": "063",
            "value": 4339
        },
        {
            "id": "065",
            "value": 2073
        },
        {
            "id": "067",
            "value": 1018
        },
        {
            "id": "069",
            "value": 3967
        },
        {
            "id": "071",
            "value": 3401
        },
        {
            "id": "073",
            "value": 3307
        },
        {
            "id": "075",
            "value": 1938
        },
        {
            "id": "077",
            "value": 489
        },
        {
            "id": "079",
            "value": 3207
        },
        {
            "id": "081",
            "value": 2295
        },
        {
            "id": "083",
            "value": 2747
        },
        {
            "id": "085",
            "value": 1114
        },
        {
            "id": "087",
            "value": 3400
        },
        {
            "id": "089",
            "value": 784
        },
        {
            "id": "091",
            "value": 1673
        },
        {
            "id": "093",
            "value": 4274
        },
        {
            "id": "095",
            "value": 4509
        },
        {
            "id": "097",
            "value": 3862
        },
        {
            "id": "099",
            "value": 1356
        },
        {
            "id": "101",
            "value": 4126
        },
        {
            "id": "103",
            "value": 1314
        },
        {
            "id": "105",
            "value": 1807
        },
        {
            "id": "107",
            "value": 4026
        },
        {
            "id": "109",
            "value": 3456
        },
        {
            "id": "111",
            "value": 1393
        },
        {
            "id": "113",
            "value": 1500
        },
        {
            "id": "115",
            "value": 2218
        }
    ]
    }
    ```

    Para renderizar el mapa anterior, primero instale el paquete fusionmaps, que contiene todos los archivos de definición de mapas, como se muestra a continuación:

    ```
        $ npm install fusionmaps
    ```
  </Tab>
</Tabs>

Después de instalar el paquete fusionmaps, el código para renderizar el mapa de California es:

<Tabs>
  <Tab title="NPM">
    El paquete fusioncharts para npm ahora se puede utilizar de dos formas diferentes:

    - Módulo ES de FusionCharts
    - Módulo CJS de FusionCharts

    **Los pasos para renderizar un mapa para ambos módulos se muestran a continuación:**

    ES6

    ```
    // Include the core fusioncharts file from core  -
    import FusionCharts from 'fusioncharts/core';

    // Include the map files
    import FusionMaps from 'fusioncharts/maps';
    import California from 'fusionmaps/maps/es/fusioncharts.california';
    // Include the fusion theme
    import FusionTheme from 'fusioncharts/themes/es/fusioncharts.theme.fusion'

    // Add the map as dependency
    // E.g. FusionCharts.addDep(ChartType)
    FusionCharts.addDep(FusionMaps);
    FusionCharts.addDep(California);
    FusionCharts.addDep(FusionTheme);

    // Create an Instance with map options
    var webVisit = new FusionCharts({
    type: 'maps/california',
    width: '800',
    height: '550',
    renderAt: 'chart-container',
    dataFormat: 'json',
    dataSource: {
    "chart": {
    "animation": "0",
    "showbevel": "0",
    "usehovercolor": "1",
    "showlegend": "1",
    "legendposition": "BOTTOM",
    "legendborderalpha": "0",
    "legendbordercolor": "ffffff",
    "legendallowdrag": "0",
    "legendshadow": "0",
    "caption": "Website Visits for the month of March 2018",
    "connectorcolor": "000000",
    "fillalpha": "80",
    "hovercolor": "CCCCCC",
    "theme": "fusion"
    },
    "colorrange": {
    "minvalue": "0",
    "startlabel": "Low",
    "endlabel": "High",
    "code": "e44a00",
    "gradient": "1",
    "color": [{"maxvalue": "2500", "code": "f8bd19"}, {"maxvalue": "5000", "code": "6baa01"}]
    },
    "data": [{"id":"001","value":2834},{"id":"003","value":3182},{"id":"005","value":3280},{"id":"007","value":911},{"id":"009","value":292},{"id":"011","value":530},{"id":"013","value":2515},{"id":"015","value":728},{"id":"017","value":1974},{"id":"019","value":848},{"id":"021","value":3278},{"id":"023","value":4463},{"id":"025","value":1198},{"id":"027","value":378},{"id":"029","value":2610},{"id":"031","value":1200},{"id":"033","value":3820},{"id":"035","value":940},{"id":"037","value":3416},{"id":"039","value":4004},{"id":"041","value":1604},{"id":"043","value":4011},{"id":"045","value":3203},{"id":"047","value":3775},{"id":"049","value":2721},{"id":"051","value":3417},{"id":"053","value":1530},{"id":"055","value":412},{"id":"057","value":3434},{"id":"059","value":1670},{"id":"061","value":1274},{"id":"063","value":4339},{"id":"065","value":2073},{"id":"067","value":1018},{"id":"069","value":3967},{"id":"071","value":3401},{"id":"073","value":3307},{"id":"075","value":1938},{"id":"077","value":489},{"id":"079","value":3207},{"id":"081","value":2295},{"id":"083","value":2747},{"id":"085","value":1114},{"id":"087","value":3400},{"id":"089","value":784},{"id":"091","value":1673},{"id":"093","value":4274},{"id":"095","value":4509},{"id":"097","value":3862},{"id":"099","value":1356},{"id":"101","value":4126},{"id":"103","value":1314},{"id":"105","value":1807},{"id":"107","value":4026},{"id":"109","value":3456},{"id":"111","value":1393},{"id":"113","value":1500},{"id":"115","value":2218}]
    }
    });
    // Render
    webVisit.render();
    ```

    CJS

    ```
    var FusionCharts = require('fusioncharts');
    var FusionMaps = require('fusioncharts/fusioncharts.maps');
    var California = require('fusionmaps/maps/fusioncharts.california');
    var FusionTheme = require('fusioncharts/themes/fusioncharts.theme.fusion');

    FusionMaps(FusionCharts);
    California(FusionCharts);
    FusionTheme(FusionCharts);

    // Create an Instance with map options
    var webVisit = new FusionCharts({
    type: 'maps/california',
    width: '800',
    height: '550',
    renderAt: 'chart-container',
    dataFormat: 'json',
    dataSource: {
    "chart": {
    "animation": "0",
    "showbevel": "0",
    "usehovercolor": "1",
    "showlegend": "1",
    "legendposition": "BOTTOM",
    "legendborderalpha": "0",
    "legendbordercolor": "ffffff",
    "legendallowdrag": "0",
    "legendshadow": "0",
    "caption": "Website Visits for the month of March 2018",
    "connectorcolor": "000000",
    "fillalpha": "80",
    "hovercolor": "CCCCCC",
    "theme": "fusion"
    },
    "colorrange": {
    "minvalue": "0",
    "startlabel": "Low",
    "endlabel": "High",
    "code": "e44a00",
    "gradient": "1",
    "color": [{"maxvalue": "2500", "code": "f8bd19"}, {"maxvalue": "5000", "code": "6baa01"}]
    },
    "data": [{"id":"001","value":2834},{"id":"003","value":3182},{"id":"005","value":3280},{"id":"007","value":911},{"id":"009","value":292},{"id":"011","value":530},{"id":"013","value":2515},{"id":"015","value":728},{"id":"017","value":1974},{"id":"019","value":848},{"id":"021","value":3278},{"id":"023","value":4463},{"id":"025","value":1198},{"id":"027","value":378},{"id":"029","value":2610},{"id":"031","value":1200},{"id":"033","value":3820},{"id":"035","value":940},{"id":"037","value":3416},{"id":"039","value":4004},{"id":"041","value":1604},{"id":"043","value":4011},{"id":"045","value":3203},{"id":"047","value":3775},{"id":"049","value":2721},{"id":"051","value":3417},{"id":"053","value":1530},{"id":"055","value":412},{"id":"057","value":3434},{"id":"059","value":1670},{"id":"061","value":1274},{"id":"063","value":4339},{"id":"065","value":2073},{"id":"067","value":1018},{"id":"069","value":3967},{"id":"071","value":3401},{"id":"073","value":3307},{"id":"075","value":1938},{"id":"077","value":489},{"id":"079","value":3207},{"id":"081","value":2295},{"id":"083","value":2747},{"id":"085","value":1114},{"id":"087","value":3400},{"id":"089","value":784},{"id":"091","value":1673},{"id":"093","value":4274},{"id":"095","value":4509},{"id":"097","value":3862},{"id":"099","value":1356},{"id":"101","value":4126},{"id":"103","value":1314},{"id":"105","value":1807},{"id":"107","value":4026},{"id":"109","value":3456},{"id":"111","value":1393},{"id":"113","value":1500},{"id":"115","value":2218}]
    }
    });
    // Render
    webVisit.render();
    ```
  </Tab>

  <Tab title="CDN">
    Para utilizar cualquier otro mapa (excepto el del Mundo y el de EE. UU.) de los más de 1600 mapas, descargue los archivos de definición de mapas y luego copie esos archivos de mapas en su carpeta de mapas actual.

    Los archivos de definición de mapas se nombran con el formato fusioncharts.\[MAP_ALIAS].js, donde MAP_ALIAS representa el nombre del país, estado o región.

    ```
    <html>
    <head>
    <!-- Including the fusioncharts core library -->
    <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.js"></script>
    <!-- Including the map renderer file -->
    <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/fusioncharts.maps.js "></script>
    <!-- Including the map definition file -->
    <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/maps/fusioncharts.california.js"></script>
    <!-- Including the fusion theme -->
    <script type="text/javascript" src="https://cdn.fusioncharts.com/fusioncharts/latest/themes/fusioncharts.theme.fusion.js"></script>
    <script type="text/javascript">
    const webVisit = {
    type: 'maps/california',
    renderAt: 'chart-container',
    width: '800',
    height: '550',
    dataFormat: 'json',
    dataSource: {
        "chart": {
            "animation": "0",
            "showbevel": "0",
            "usehovercolor": "1",
            "showlegend": "1",
            "legendposition": "BOTTOM",
            "legendborderalpha": "0",
            "legendbordercolor": "ffffff",
            "legendallowdrag": "0",
            "legendshadow": "0",
            "caption": "Website Visits for the month of March 2018",
            "connectorcolor": "000000",
            "fillalpha": "80",
            "hovercolor": "CCCCCC",
            "theme": "fusion"
        },
        "colorrange": {
            "minvalue": "0",
            "startlabel": "Low",
            "endlabel": "High",
            "code": "e44a00",
            "gradient": "1",
            "color": [{"maxvalue": "2500", "code": "f8bd19"}, {"maxvalue": "5000", "code": "6baa01"}]
        },
        "data": [{"id":"001","value":2834},{"id":"003","value":3182},{"id":"005","value":3280},{"id":"007","value":911},{"id":"009","value":292},{"id":"011","value":530},{"id":"013","value":2515},{"id":"015","value":728},{"id":"017","value":1974},{"id":"019","value":848},{"id":"021","value":3278},{"id":"023","value":4463},{"id":"025","value":1198},{"id":"027","value":378},{"id":"029","value":2610},{"id":"031","value":1200},{"id":"033","value":3820},{"id":"035","value":940},{"id":"037","value":3416},{"id":"039","value":4004},{"id":"041","value":1604},{"id":"043","value":4011},{"id":"045","value":3203},{"id":"047","value":3775},{"id":"049","value":2721},{"id":"051","value":3417},{"id":"053","value":1530},{"id":"055","value":412},{"id":"057","value":3434},{"id":"059","value":1670},{"id":"061","value":1274},{"id":"063","value":4339},{"id":"065","value":2073},{"id":"067","value":1018},{"id":"069","value":3967},{"id":"071","value":3401},{"id":"073","value":3307},{"id":"075","value":1938},{"id":"077","value":489},{"id":"079","value":3207},{"id":"081","value":2295},{"id":"083","value":2747},{"id":"085","value":1114},{"id":"087","value":3400},{"id":"089","value":784},{"id":"091","value":1673},{"id":"093","value":4274},{"id":"095","value":4509},{"id":"097","value":3862},{"id":"099","value":1356},{"id":"101","value":4126},{"id":"103","value":1314},{"id":"105","value":1807},{"id":"107","value":4026},{"id":"109","value":3456},{"id":"111","value":1393},{"id":"113","value":1500},{"id":"115","value":2218}]
    }
    };
    // Render
    webVisit.render();
    </script>
    </head>
    </html>
    ```
  </Tab>

  <Tab title="Archivos locales">
    Para utilizar cualquier otro mapa (excepto el del Mundo y el de EE. UU.) de los más de 1600 mapas, descargue los archivos de definición de mapas y luego copie esos archivos de mapas en su carpeta de mapas actual.

    Los archivos de definición de mapas se nombran con el formato fusioncharts.\[MAP_ALIAS].js, donde MAP_ALIAS representa el nombre del país, estado o región.

    ```
    <html>
    <head>
    <!-- Including the fusioncharts core library -->
    <script type="text/javascript" src="path/to/local/fusioncharts.js"></script>
    <!-- Including the map renderer file -->
    <script type="text/javascript" src="path/to/local/fusioncharts.maps.js "></script>
    <!-- Including the map definition file -->
    <script type="text/javascript" src="path/to/local/fusioncharts.california.js"></script>
    <!-- Including the fusion theme -->
    <script type="text/javascript" src="path/to/local/themes/fusioncharts.theme.fusion.js"></script>
    <script type="text/javascript">
    const webVisit = {
    type: 'maps/california',
    renderAt: 'chart-container',
    width: '800',
    height: '550',
    dataFormat: 'json',
    dataSource: {
        "chart": {
            "animation": "0",
            "showbevel": "0",
            "usehovercolor": "1",
            "showlegend": "1",
            "legendposition": "BOTTOM",
            "legendborderalpha": "0",
            "legendbordercolor": "ffffff",
            "legendallowdrag": "0",
            "legendshadow": "0",
            "caption": "Website Visits for the month of March 2018",
            "connectorcolor": "000000",
            "fillalpha": "80",
            "hovercolor": "CCCCCC",
            "theme": "fusion"
        },
        "colorrange": {
            "minvalue": "0",
            "startlabel": "Low",
            "endlabel": "High",
            "code": "e44a00",
            "gradient": "1",
            "color": [{"maxvalue": "2500", "code": "f8bd19"}, {"maxvalue": "5000", "code": "6baa01"}]
        },
        "data": [{"id":"001","value":2834},{"id":"003","value":3182},{"id":"005","value":3280},{"id":"007","value":911},{"id":"009","value":292},{"id":"011","value":530},{"id":"013","value":2515},{"id":"015","value":728},{"id":"017","value":1974},{"id":"019","value":848},{"id":"021","value":3278},{"id":"023","value":4463},{"id":"025","value":1198},{"id":"027","value":378},{"id":"029","value":2610},{"id":"031","value":1200},{"id":"033","value":3820},{"id":"035","value":940},{"id":"037","value":3416},{"id":"039","value":4004},{"id":"041","value":1604},{"id":"043","value":4011},{"id":"045","value":3203},{"id":"047","value":3775},{"id":"049","value":2721},{"id":"051","value":3417},{"id":"053","value":1530},{"id":"055","value":412},{"id":"057","value":3434},{"id":"059","value":1670},{"id":"061","value":1274},{"id":"063","value":4339},{"id":"065","value":2073},{"id":"067","value":1018},{"id":"069","value":3967},{"id":"071","value":3401},{"id":"073","value":3307},{"id":"075","value":1938},{"id":"077","value":489},{"id":"079","value":3207},{"id":"081","value":2295},{"id":"083","value":2747},{"id":"085","value":1114},{"id":"087","value":3400},{"id":"089","value":784},{"id":"091","value":1673},{"id":"093","value":4274},{"id":"095","value":4509},{"id":"097","value":3862},{"id":"099","value":1356},{"id":"101","value":4126},{"id":"103","value":1314},{"id":"105","value":1807},{"id":"107","value":4026},{"id":"109","value":3456},{"id":"111","value":1393},{"id":"113","value":1500},{"id":"115","value":2218}]
    }
    };
    // Render
    webVisit.render();
    </script>
    </head>
    </html>
    ```
  </Tab>
</Tabs>

¡Eso es todo! El mapa de **California** está listo.

## ¿Problemas para renderizar el gráfico? {#problem-rendering-the-chart}

En caso de que ocurra un error y no pueda ver el gráfico, verifique lo siguiente:

- Si recibe un error de JavaScript en su página, revise la consola de su navegador para ver el error exacto y corríjalo en consecuencia. Si no puede resolverlo, haga clic [aquí](https://www.fusioncharts.com/contact-support) para ponerse en contacto con nuestro equipo de soporte.

- Si el gráfico no se muestra en absoluto, pero no hay errores de JavaScript, verifique si la biblioteca JavaScript de FusionCharts Suite XT se ha cargado correctamente. Puede utilizar las herramientas de desarrollo de su navegador para comprobar si se cargó `fusioncharts.js`.

- Si recibe un mensaje de **Cargando datos** o **Error al cargar datos**, verifique si la estructura de sus datos JSON es correcta o si existen conflictos relacionados con las comillas en su código.
