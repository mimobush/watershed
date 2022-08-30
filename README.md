# watershed
var watershed = ee.FeatureCollection("WWF/HydroSHEDS/v1/Basins/hybas_4").filterBounds(ROI);
Map.addLayer(watershed, {}, 'colored');
Export.image.toDrive(watershed, "WestPokot_Watershed", "shp");
