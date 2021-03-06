# Google Earth Engine plugin for QGIS

Integrates Google Earth Engine with QGIS using Python API. 

Check [User Guide](https://gee-community.github.io/qgis-earthengine-plugin/) to get started.

[![Gitter](https://badges.gitter.im/gee-community/qgis-earthengine-plugin.svg)](https://gitter.im/gee-community/qgis-earthengine-plugin?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

![Add Sentinel-2 image](https://raw.githubusercontent.com/gee-community/qgis-earthengine-plugin/master/media/add_map_layer.png)

### Roadmap

#### Alpha 0.1 (Q4 2019)
- [x] Create a new QGIS plugin skeleton
- [x] Migrate to QGIS3
- [x] Embed GEE Python library
- [x] Implement Map.addLayer() for ee.Image
- [x] Implement Map.addLayer() for ee.Geometry, ee.Feature and ee.FeatureCollection
- [x] Implement Map.centerObject()
- [x] Implement Map.getBounds()
- [x] Implement Map.getCenter()
- [x] Implement Map.setCenter()
- [x] Implement Map.getScale()
- [x] Implement Map.getZoom()
- [x] Implement Map.setZoom()
- [ ] Upload to QGIS plugin repository: https://plugins.qgis.org/plugins/

#### Alpha 0.2 (Q1 2020)
- [ ] EE layer inspector
- [ ] Make print(ee_object) more user-friendly, without requiring getInfo(), maybe async
...

#### Beta
- [ ] Add support for map layers in a way similar to EE Code Editor
- [ ] Add support for Data Catalog, allowing adding assets without the need to write scripts (select time, styling)
- [ ] Custom EE scripts as Processing algorithms, so that users can use it within Graphical Modeller
- [ ] Fetch (cache?) raster assets locally (EE > QGIS), for a given rectangle / CRS, as a Processing tool
- [ ] Export vector and raster data (QGIS > EE) either via Tasks or some other way
- [ ] Use QGIS vector/raster style editors to edit EE layer styles

## Contributors
[![@gena](https://github.com/gena.png?size=40 "Gena")](http://github.com/gena)
[![@XavierCLL](https://github.com/XavierCLL.png?size=40 "Xavier")](http://github.com/XavierCLL)
[![@hcwinsemius](https://github.com/github.png?size=40 "Hessel")](http://github.com/hcwinsemius)
[![@siggyf](https://github.com/siggyf.png?size=40 "Fedor")](http://github.com/siggyf)

### For Developers

This section is for developers-only. 

The ee_plugin uses paver for packaging. If you do not have paver (https://github.com/paver/paver) installed, install it by typing the following in a console:

```pip install paver```

Open a console in the folder created in the first step, and type

```paver setup```

This will get all the dependencies needed by the plugin.

Install into QGIS by running

```paver install```

This should create a symbolic link to the plugin directory wihin the QGIS plugins deployment directory. Check Settings > User Profiles > Open Active Profile Folder, and then go to python/plugins. To reload any changes made in the plugin into Qgis, it is recommended to use the [plugin reloader](https://plugins.qgis.org/plugins/plugin_reloader/).

To generate the installable zip package

```paver package``` 

### Random Links

* [Ujaval Gandhi](https://twitter.com/spatialthoughts) - [QGIS Plugin Builder](http://g-sherman.github.io/Qgis-Plugin-Builder/)
* JetBrains - [PyCharm](https://www.jetbrains.com/pycharm/)


