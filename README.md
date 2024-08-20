# MapTiler Dark Mode XYZ Tiles

This repository provides Dark Mode tiles, which offer a visually appealing and easy-on-the-eyes dark-themed map style. Dark Mode is ideal for use in applications that require low-light conditions or a modern, sleek appearance. These tiles are compatible with any GIS software that supports XYZ tile layers, making them versatile for various mapping applications.

## Features

- **Dark Mode Theme:** Aesthetically pleasing dark-themed map tiles for better visibility in low-light conditions.
- **High Compatibility:** Supports integration with popular GIS software like QGIS, ArcGIS, Leaflet, OpenLayers, and more.
- **Customizable:** Easily adaptable to fit various application needs, including web maps and desktop GIS projects.

## How to Configure XYZ Tiles in GIS Software

To use these tiles in your GIS software, you'll need to add an XYZ tile layer. Below are the general steps:

### QGIS

1. Open QGIS and go to **Layer** > **Add Layer** > **Add XYZ Layer**.
2. In the dialog that appears, enter the following details:
   - **Name:** Dark Mode
   - **URL:** `https://github.com/Chillystout/tileserver/raw/main/DarkMode/{z}/{x}/{y}.png`
3. Click **OK** to add the layer to your project.

### ArcGIS

1. Open ArcGIS Pro or ArcMap.
2. Go to **Catalog Pane** > **Project** > **Add Data** > **Add Data From Path**.
3. Enter the following URL in the dialog:
   - `https://github.com/Chillystout/tileserver/raw/main/DarkMode/{z}/{x}/{y}.png`
4. Click **Add** to include the tile layer in your map.

### Leaflet

To add the tiles in a Leaflet web map:

```javascript
var map = L.map('map').setView([51.505, -0.09], 13);

L.tileLayer('https://github.com/Chillystout/tileserver/raw/main/DarkMode/{z}/{x}/{y}.png', {
    maxZoom: 18,
    attribution: 'Map data &copy; <a href="https://www.maptiler.com/">MapTiler</a>'
}).addTo(map);
```

### OpenLayers

To add the tiles in an OpenLayers map:

```javascript
var map = new ol.Map({
    target: 'map',
    layers: [
        new ol.layer.Tile({
            source: new ol.source.XYZ({
                url: 'https://your-tile-server-url/{z}/{x}/{y}.png'
            })
        })
    ],
    view: new ol.View({
        center: ol.proj.fromLonLat([0, 0]),
        zoom: 2
    })
});
```

### Buy Me a Coffee
If you find this project useful and would like to support its development, consider buying me a coffee! Your support helps keep the project going and motivates future updates.

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/chillystout)

### License
This project is licensed under the MIT License - see the LICENSE file for details.