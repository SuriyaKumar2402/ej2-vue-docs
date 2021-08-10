---
title: " Customization in Vue Maps control | Syncfusion "

component: "Maps"

description: "Learn here all about Customization of Syncfusion Vue Maps control and more."
---

# Customization in Vue Maps control

## Setting the size for Maps

The width and height of the Maps can be set using the [`width`](../api/maps/mapsModel/#width) and [`height`](../api/maps/mapsModel/#height) properties in the Maps control. Percentage or pixel values can be used for the height and width values.

{% tab template= "maps/getting-started", isDefaultActive=true %}

```html
<template>
    <div id="map">
        <div class='wrapper'>
            <ejs-maps height='300px' width='200px'>
                <e-layers>
                    <e-layer :shapeData='shapeData'></e-layer>
                </e-layers>
            </ejs-maps>
        </div>
    </div>
</template>
<script>
import Vue from 'vue';
import { MapsPlugin } from '@syncfusion/ej2-vue-maps';
import { world_map } from './world-map.js';
Vue.use(MapsPlugin);
export default {
    data () {
        return {
            shapeData: world_map
        }
    }
}
</script>
<style>
  .wrapper {
    max-width: 400px;
    margin: 0 auto;
  }
</style>
```

{% endtab %}

## Maps title

The title for the Maps can be set using the [`titleSettings`](../api/maps/titleSettingsModel/) property. It can be customized using the following properties.

* [`alignment`](../api/maps/titleSettingsModel/#alignment) - To customize the alignment for the text in the title for the Maps. The possible values are "**Center**", "**Near**" and "**Far**".
* [`description`](../api/maps/titleSettingsModel/#description) - To set the description of the title in Maps.
* [`text`](../api/maps/titleSettingsModel/#text) - To set the text for the title in Maps.
* [`textStyle`](../api/maps/titleSettingsModel/#textstyle) - To customize the text of the title in Maps.
* [`subtitleSettings`](../api/maps/titleSettingsModel/#subtitlesettings) - To customize the subtitle for the Maps.

{% tab template= "maps/getting-started", isDefaultActive=true %}

```html
<template>
    <div id="map">
        <div class='wrapper'>
            <ejs-maps :titleSettings='titleSettings'>
                <e-layers>
                    <e-layer :shapeData='shapeData' :shapeSettings='shapeSettings'></e-layer>
                </e-layers>
            </ejs-maps>
        </div>
    </div>
</template>
<script>
import Vue from 'vue';
import { MapsPlugin } from '@syncfusion/ej2-vue-maps';
import { world_map } from './world-map.js';
Vue.use(MapsPlugin);
export default {
    data () {
        return {
            titleSettings: {
                text: 'Maps Component',
                textStyle: {
                    color: 'red',
                    fontStyle: 'italic',
                    fontWeight: 'regular',
                    fontFamily: 'arial',
                    size: '14px'
                },
                alignment: 'Center'
            },
            shapeData: world_map,
            shapeSettings: {
                autofill: true
            }
        }
    }
}
</script>
<style>
  .wrapper {
    max-width: 400px;
    margin: 0 auto;
  }
</style>
```

{% endtab %}

## Setting theme

The Maps control supports following themes.

* Material
* Fabric
* Bootstrap
* Highcontrast
* MaterialDark
* FabricDark
* BootstrapDark
* Bootstrap4
* HighContrastLight
* Tailwind

By default, the Maps are rendered by the **"Material"** theme. The theme of the Maps component is changed using the [`theme`](../api/maps/mapsModel/#theme) property.

{% tab template= "maps/getting-started", isDefaultActive=true %}

```html
<template>
    <div id="map">
        <div class='wrapper'>
            <ejs-maps theme="MaterialDark">
                <e-layers>
                    <e-layer :shapeData='shapeData'></e-layer>
                </e-layers>
            </ejs-maps>
        </div>
    </div>
</template>
<script>
import Vue from 'vue';
import { MapsPlugin } from '@syncfusion/ej2-vue-maps';
import { world_map } from './world-map.js';
Vue.use(MapsPlugin);
export default {
    data () {
        return {
            shapeData: world_map
        }
    }
}
</script>
<style>
  .wrapper {
    max-width: 400px;
    margin: 0 auto;
  }
</style>
```

{% endtab %}

## Customizing Maps container

The following properties are available to customize the container in the Maps.

* [`background`](../api/maps/mapsModel/#background) - To apply the background color to the container in the Maps.
* [`border`](../api/maps/mapsModel/#border) - To customize the color, width and opacity of the border of the Maps.
* [`margin`](../api/maps/mapsModel/#margin) - To customize the margins of the Maps.

{% tab template= "maps/getting-started", isDefaultActive=true %}

```html
<template>
    <div id="map">
        <div class='wrapper'>
            <ejs-maps :background='background' :border='border' :margin='margin'>
                <e-layers>
                    <e-layer :shapeData='shapeData' :shapeSettings='shapeSettings'></e-layer>
                </e-layers>
            </ejs-maps>
        </div>
    </div>
</template>
<script>
import Vue from 'vue';
import { MapsPlugin } from '@syncfusion/ej2-vue-maps';
import { world_map } from './world-map.js';
Vue.use(MapsPlugin);
export default {
    data () {
        return {
            shapeData: world_map,
            background: '#CCD1D1',
            border: {
                color: 'green',
                width: 2
            },
            margin: {
                bottom: 10,
                left: 20,
                right: 20,
                top: 10
            },
            shapeSettings: {
                autofill: true
            }
        }
    }
}
</script>
<style>
  .wrapper {
    max-width: 400px;
    margin: 0 auto;
  }
</style>
```

{% endtab %}

## Customizing Maps area

By default, the background color of the shape maps is set as white. To modify the background color of the Maps area, the [`background`](../api/maps/mapsAreaSettingsModel/#background) property in the [`mapsArea`](../api/maps/mapsAreaSettingsModel) is used. The border of the Maps area can be customized using the [`border`](../api/maps/mapsAreaSettingsModel/#border) property in the [`mapsArea`](../api/maps/mapsAreaSettingsModel) property.

{% tab template= "maps/getting-started", isDefaultActive=true %}

```html
<template>
    <div id="map">
        <div class='wrapper'>
            <ejs-maps :mapsArea='mapsArea'>
                <e-layers>
                    <e-layer :shapeData='shapeData' :shapeSettings='shapeSettings'></e-layer>
                </e-layers>
            </ejs-maps>
        </div>
    </div>
</template>
<script>
import Vue from 'vue';
import { MapsPlugin } from '@syncfusion/ej2-vue-maps';
import { world_map } from './world-map.js';
Vue.use(MapsPlugin);
export default {
    data () {
        return {
            shapeData: world_map,
            mapsArea: {
                background: '#CCD1D1',
                border: {
                    width: 2,
                    color: 'green'
                }
            },
            shapeSettings: {
                autofill: true,
            }
        }
    }
}
</script>
<style>
  .wrapper {
    max-width: 400px;
    margin: 0 auto;
  }
</style>
```

{% endtab %}

## Customizing the shapes

The following properties are available in [`shapeSettings`](../api/maps/shapeSettingsModel/) property to customize the shapes of the Maps component.

* [`fill`](../api/maps/shapeSettingsModel/#fill) - To apply the color to the shapes.
* [`autofill`](../api/maps/shapeSettingsModel/#autofill) - To apply the palette colors to the shapes if it is set as true.
* [`palette`](../api/maps/shapeSettingsModel/#palette) - To set the custom palette for the shapes.
* [`border`](../api/maps/shapeSettingsModel/#border) - To customize the color, width and opacity of the border of the shapes.
* [`dashArray`](../api/maps/shapeSettingsModel/#dasharray) - To define the pattern of dashes and gaps that is applied to the outline of the shapes.
* [`opacity`](../api/maps/shapeSettingsModel/#opacity) - To customize the transparency for the shapes.

{% tab template= "maps/getting-started", isDefaultActive=true %}

```html
<template>
    <div id="map">
        <div class='wrapper'>
            <ejs-maps >
                <e-layers>
                    <e-layer :shapeData='shapeData' :shapeSettings='shapeSettings' :layerType='layerType' ></e-layer>
                </e-layers>
            </ejs-maps>
        </div>
    </div>
</template>
<script>
import Vue from 'vue';
import { MapsPlugin } from '@syncfusion/ej2-vue-maps';
import { world_map } from './world-map.js';
Vue.use(MapsPlugin);
export default {
data () {
    return {
        shapeData: world_map,
        shapeSettings: {
            autofill: true,
            palette: ['#33CCFF', '#FF0000', '#800000', '#FFFF00', '#808000'],
            border: {
                color: 'green',
                width: 2
            },
            dashArray: '1',
            opacity: 0.9
        }
    }
}
}
</script>
<style>
  .wrapper {
    max-width: 400px;
    margin: 0 auto;
  }
</style>
```

{% endtab %}

## Setting color to the shapes from the data source

The color for each shape in the Maps can be set using the [`colorValuePath`](../api/maps/shapeSettingsModel/#colorvaluepath) property of [`shapeSettings`](../api/maps/shapeSettingsModel/) property. The value for the [`colorValuePath`](../api/maps/shapeSettingsModel/#colorvaluepath) property is the field name from the data source of the [`shapeSettings`](../api/maps/shapeSettingsModel/) property which contains the color values.

{% tab template= "maps/getting-started", isDefaultActive=true %}

```html
<template>
    <div id="map">
        <div class='wrapper'>
            <ejs-maps>
                <e-layers>
                    <e-layer :shapeData='shapeData' :layerType='layerType' :shapePropertyPath='shapePropertyPath'
                             :shapeDataPath='shapeDataPath' :dataSource='dataSource' :shapeSettings='shapeSettings'></e-layer>
                </e-layers>
            </ejs-maps>
        </div>
    </div>
</template>
<script>
import Vue from 'vue';
import { MapsPlugin } from '@syncfusion/ej2-vue-maps';
import { world_map } from './world-map.js';
Vue.use(MapsPlugin);
export default {
    data () {
        return {
            shapeData: world_map,
            shapePropertyPath: 'continent',
            shapeDataPath: 'continent',
            dataSource: [
                { continent: "North America", color: '#71B081' },
                { continent: "South America", color: '#5A9A77' },
                { continent: "Africa", color: '#498770' },
                { continent: "Europe", color: '#39776C' },
                { continent: "Asia", color: '#266665' },
                { continent: "Oceania", color: '#124F5E' }
            ],
            shapeSettings: {
                colorValuePath: 'color',
            }
        }
    }
}
</script>
<style>
  .wrapper {
    max-width: 400px;
    margin: 0 auto;
  }
</style>
```

{% endtab %}

## Applying border to individual shapes

The border of each shape in the Maps can be customized using the [`borderColorValuePath`](../api/maps/shapeSettingsModel/#bordercolorvaluepath) and [`borderWidthValuePath`](../api/maps/shapeSettingsModel/#borderwidthvaluepath) properties to modify the color and the width of the border respectively. The field name in the data source of the layer which contains the color and the width values must be set in the [`borderColorValuePath`](../api/maps/shapeSettingsModel/#bordercolorvaluepath) and [`borderWidthValuePath`](../api/maps/shapeSettingsModel/#borderwidthvaluepath) properties respectively. If the values of [`borderColorValuePath`](../api/maps/shapeSettingsModel/#bordercolorvaluepath) and [`borderWidthValuePath`](../api/maps/shapeSettingsModel/#borderwidthvaluepath) do not match with the field name from the data source, then the color and width of the border will be applied to the shapes using the border property in the [`shapeSettings`](../api/maps/shapeSettingsModel/) property.

{% tab template= "maps/getting-started", isDefaultActive=true %}

```html
<template>
    <div id="map">
        <div class='wrapper'>
            <ejs-maps>
                <e-layers>
                    <e-layer :shapeData='shapeData' :layerType='layerType' :shapePropertyPath='shapePropertyPath'
                             :shapeDataPath='shapeDataPath' :dataSource='dataSource' :shapeSettings='shapeSettings'></e-layer>
                </e-layers>
            </ejs-maps>
        </div>
    </div>
</template>
<script>
import Vue from 'vue';
import { MapsPlugin } from '@syncfusion/ej2-vue-maps';
import { world_map } from './world-map.js';
Vue.use(MapsPlugin);
export default {
    data () {
        return {
            shapeData: world_map,
            shapePropertyPath: 'continent',
            shapeDataPath: 'continent',
            dataSource: [
                { continent: "North America", color: '#71B081', borderColor: '#CCFFE5', width: 2 },
                { continent: "South America", color: '#5A9A77', borderColor: 'red', width: 2 },
                { continent: "Africa", color: '#498770', borderColor: '#FFCC99', width: 2 },
                { continent: "Europe", color: '#39776C', borderColor: '#66B2FF', width: 2 },
                { continent: "Asia", color: '#266665', borderColor: '#999900', width: 2 },
                { continent: "Oceania", color: '#124F5E', borderColor: 'blue', width: 2 }
            ],
            shapeSettings: {
                borderColorValuePath: 'borderColor',
                borderWidthValuePath: 'width',
                colorValuePath: 'color'
            }
        }
    }
}
</script>
<style>
  .wrapper {
    max-width: 400px;
    margin: 0 auto;
  }
</style>
```

{% endtab %}

## Projection type

The Maps control supports the following projection types:

* Mercator
* Equirectangular
* Miller
* Eckert3
* Eckert5
* Eckert6
* Winkel3
* AitOff

By default, the Maps are rendered by the "**Mercator**" projection type in which the Maps are rendered based on the coordinates. So, the Maps is not stretched. To change the type of projection in the Maps, the [`projectionType`](../api/maps/mapsModel/#projectiontype) property is used.

{% tab template= "maps/getting-started", isDefaultActive=true %}

```html
<template>
    <div id="map">
        <div class='wrapper'>
            <ejs-maps projectionType= 'Miller'>
                <e-layers>
                    <e-layer :shapeData='shapeData' :shapeSettings='shapeSettings' :layerType='layerType' ></e-layer>
                </e-layers>
            </ejs-maps>
        </div>
    </div>
</template>
<script>
import Vue from 'vue';
import { MapsPlugin } from '@syncfusion/ej2-vue-maps';
import { world_map } from './world-map.js';
Vue.use(MapsPlugin);
export default {
data () {
    return {
        shapeData: world_map,
        shapeSettings: {
            autofill: true,
            palette: ['#33CCFF', '#FF0000', '#800000', '#FFFF00', '#808000']
        }
    }
}
}
</script>
<style>
  .wrapper {
    max-width: 400px;
    margin: 0 auto;
  }
</style>
```

{% endtab %}