OpenLayers 3 - Advanced styles with the canvas renderer
This JavaScript file allows OpenLayers 3 users to assign an image property to the fill object.
No mater the image size, it will repeatedly fill the feature which has the advanced style.
Version: v1.0
-------------------------------------------------------------------------------------------------------------
How to include : 
To use the ol-aswcr.js file, you have to include it in your html page AFTER the ol JavaScript file including.

<html>
	<head>
		...
	</head>
	<body>
		...
		<script src="../Ressources/ol-debug.js" type="text/javascript"></script>
        <script src="../Ressources/ol-aswcr.js" type="text/javascript"></script>
		
		<script>
			...Your script...
		</script>
	</body>
</html>

-------------------------------------------------------------------------------------------------------------
How to style :
the 'image' property of the fill object is an array : [imageObject, opacityNumber]

imageObject : the image object with which you want to fill features
opacityNumber : the transparency intensity, number between 0 and 1, in which 0 is fully transparent and 1 is fully opaque

<script>
	var img = new Image();
	img.src = 'yourImagePath';

	var yourStyle = [new ol.style.Style({
		fill: new ol.style.Fill({
			image: [img, 0.4]
		}),
		stroke: new ol.style.Stroke({
			color: "black",
			width: 2
		})
	})];
</script>