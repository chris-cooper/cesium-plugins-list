cesium-GeoserverTerrainProvider
================

GeoserverTerrainProvider: A terrain provider which works with geoserver providing elevation datas in bil, png, gif and jpeg formats. The bil format sholud be favour. 

#Cesium version: 
Tested against b24.

License: Apache 2.0. Free for commercial and non-commercial use. See LICENSE.md.

#Usage:

- Import the GeoserverTerrainProvider.js file into your html codes after importing Cesium.js.
- Create a new instance of GeoserverTerrainProvider with url of your geoserver and name of elevation layer.

After that, the GeoserverTerrainProvider will determine the capabilities of geoserver (WMS request getCapabilities) and will be ready to provide terrain data.

#Example

    <script src="/path/to/Cesium.js" type="text/javascript"></script>
    <script src="/path/to/GeoserverTerrainProvider.js" type="text/javascript"></script>
    <body>
	<canvas id="cesiumContainer"></canvas>
	<script>
		var canvas = document.getElementById('@conteneurCesium');
		var scene = new Cesium.Scene(canvas);
		var primitives = scene.getPrimitives();
		var centralBody = new Cesium.CentralBody(Cesium.Ellipsoid.WGS84);
		primitives.setCentralBody(centralBody);
		var terrainProvider = new Cesium.GeoserverTerrainProvider({
	        url : "http://localhost:8080/geoserver/elevation/wms",
	        layerName: "SRTM90",
	        heightmapWidth:64
	    });
	  centralBody.terrainProvider = terrainProvider; 
	</script>
    </body>
Where
- "http://localhost:8080/geoserver/elevation/wms" is the url to go to the wms of "elevation" workspace stored in geoserver;
- "SRTM90" is the name of the layer in "elevation" workspace
- "64" is size of terrain cells request by GeoserverTerrainProvider
 

