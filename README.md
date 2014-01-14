<p align="center">
<a href="http://cesium.agi.com/">
<img src="https://github.com/AnalyticalGraphicsInc/cesium/wiki/logos/Cesium_Logo_Color.jpg" width="50%" />
</a>
</p>

This repo contains the list of Cesium plugins used to generate the plugin list on [cesiumjs.org](http://cesiumjs.org/plugins).  Open a pull request to add yours.

**What is a Cesium plugin?**

A Cesium plugin is a library that integrates with Cesium to add functionality.  Developers build apps using core Cesium and any additional plugins.  For example, [cesium-leap](https://github.com/Aviture/cesium-leap) is a plugin that adds support for navigation with the [Leap Motion controller](https://www.leapmotion.com/), and [cesium-materials-pack](https://github.com/AnalyticalGraphicsInc/cesium-materials-pack) is a plugin that adds new materials like brick and wood patterns.

A plugin may extend Cesium by extending Cesium types like [imagery providers](http://cesiumjs.org/2013/01/04/Cesium-Imagery-Layers-Tutorial/), [terrain providers](http://cesiumjs.org/2013/02/15/Cesium-Terrain-Tutorial/), [geometries](http://cesiumjs.org/2013/11/04/Geometry-and-Appearances/), [appearances](http://cesiumjs.org/2013/11/04/Geometry-and-Appearances/), etc.  A plugin may also create new functionality by building on top of Cesium, even something as simple as a new numeric library built using Cesium math types.  Some plugins aren't even strictly JavaScript libraries; for example, [cesium-starter-app](https://github.com/pjcozzi/cesium-starter-app) provides a starter app for quick hacking, and [cesium-assets](https://github.com/AnalyticalGraphicsInc/cesium-assets) is a collection of useful graphics assets such as imagery and stars.  The common theme is that plugins add value to Cesium-based apps.

**How do I use plugins?**

Plugins are listed on [cesiumjs.org](http://cesiumjs.org/plugins).  Each plugin has documentation for installing and using it.  Getting started can be as simple as including a `.js` file in your html.

**How do I list my plugin with the plugins on cesium.js?**

Fork this repo, add your plugin to [index.html](index.html) and images to a new subdirectory in [images](images/), and open a pull request.  We'll review and merge it promptly and your plugin will soon be listed on cesiumjs.org.  We'll also help promote your plugin on the cesium  [forum](http://cesiumjs.org/forum.html), [blog](http://cesiumjs.org/blog.html), and [twitter](https://twitter.com/cesiumjs).

We ask that each plugin follow these three simple guidelines:

* State what version(s) of Cesium it is compatiable with.
* State what license it uses and the licenses of any third-party code.  Cesium uses [Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0.html), which may be a good choice for your plugin.  Although we expect most plugins will be open-source, closed-source plugins are allowed.
* Include documentation on how to install and use it.  For small plugins, this is as simple as a README.md.

To make your plugin awesome, we also suggest:

* Use github for hosting and name the repo starting with `cesium-`.
* Include a hosted demo.  With github, this can be done with a `gh-pages` branch ([tutorial](http://xlson.com/2010/11/09/getting-started-with-github-pages.html)).
* Use the Cesium coding conventions for the plugin's public interfaces so it is consistent with Cesium and other plugins.
* Keep the plugin up-to-date if new versions of Cesium contain breaking changes.  This will ensure the continued popularity of your plugin.
* Include contact info for getting help with the plugin, perhaps a forum link or email address.
* Include unit tests.

The [cesium-materials-pack](https://github.com/AnalyticalGraphicsInc/cesium-materials-pack) plugin is a good example to follow.

**What's the difference between a plugin and a core Cesium feature?**

A plugin lives outside the main [Cesium repo](https://github.com/AnalyticalGraphicsInc/cesium) and is developed and licensed separately.  Creating a plugin does not require the Cesium [Contributor License Agreement](https://github.com/AnalyticalGraphicsInc/cesium/blob/master/CONTRIBUTING.md) (CLA) or strictly following the Cesium coding, testing, and documentation conventions.  A plugin may also contain functionality that is not core to Cesium or third-party dependencies that would increase the size of Cesium too much to include by default.

If you have a plugin that would make a good core Cesium feature, let us know on the [forum](http://cesiumjs.org/forum.html).  A core Cesium feature has the benefit of being maintained with Cesium itself and included in the each release.
