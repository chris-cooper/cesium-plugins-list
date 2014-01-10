<p align="center">
<a href="http://cesium.agi.com/">
<img src="https://github.com/AnalyticalGraphicsInc/cesium/wiki/logos/Cesium_Logo_Color.jpg" width="50%" />
</a>
</p>

This repo contains the list of Cesium plugins used to generate the plugin list on [cesiumjs.org](http://cesiumjs.org/).  Open a pull request to add your plugin.

**What is a Cesium plugin?**

A Cesium plugin is a library that integrates with Cesium to add functionality.  Developers build apps using core Cesium and any additional plugins.  For example, [cesium-leap](https://github.com/Aviture/cesium-leap) is a plugin that adds support for navigation with the [Leap Motion controller](https://www.leapmotion.com/), and [cesium-materials-pack](https://github.com/AnalyticalGraphicsInc/cesium-materials-pack) is a plugin that adds new materials like brick and wood patterns.

A plugin may extend Cesium functionality by extending Cesium types like [imagery providers](http://cesiumjs.org/2013/01/04/Cesium-Imagery-Layers-Tutorial/), [terrain providers](http://cesiumjs.org/2013/02/15/Cesium-Terrain-Tutorial/), [geometries](http://cesiumjs.org/2013/11/04/Geometry-and-Appearances/), [appearances](http://cesiumjs.org/2013/11/04/Geometry-and-Appearances/), etc.  A plugin may also create new functionality by building on top of Cesium, even something as simple as a new numeric library built using Cesium math types.  Some plugins aren't even strictly JavaScript libraries; for example, [cesium-starter-app](https://github.com/pjcozzi/cesium-starter-app) provides a starter app for quick hacking, and [cesium-assets](https://github.com/AnalyticalGraphicsInc/cesium-assets) is a collection of useful graphics assets including imagery and stars.  The common theme is that plugins add value to Cesium-based apps.

**How do I use plugins?**

Plugins are listed on [cesiumjs.org](http://cesiumjs.org/).  Each plugin has documentation for setting it up and using it.  Getting started can be as simple as include a `.js` in your app.

**How do I create a plugin?**

TODO
